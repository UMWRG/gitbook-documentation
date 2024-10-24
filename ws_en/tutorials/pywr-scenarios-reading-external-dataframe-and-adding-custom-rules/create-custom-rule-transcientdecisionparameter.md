# Create Custom Rule - TranscientDecisionParameter

## Register Custom Rule - TranscientDecisionParameter



<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

Paste the following code and then click on the save button ![](<../../.gitbook/assets/image (51).png>)

```python
class TransientDecisionParameter(Parameter):
    """ Return one of two values depending on the current time-step

    This `Parameter` can be used to model a discrete decision event
     that happens at a given date. Prior to this date the `before`
     value is returned, and post this date the `after` value is returned.

    Parameters
    ----------
    decision_date : string or pandas.Timestamp
        The trigger date for the decision.
    before_parameter : Parameter
        The value to use before the decision date.
    after_parameter : Parameter
        The value to use after the decision date.
    earliest_date : string or pandas.Timestamp or None
        Earliest date that the variable can be set to. Defaults to `model.timestepper.start`
    latest_date : string or pandas.Timestamp or None
        Latest date that the variable can be set to. Defaults to `model.timestepper.end`
    decision_freq : pandas frequency string (default 'AS')
        The resolution of feasible dates. For example 'AS' would create feasible dates every
        year between `earliest_date` and `latest_date`. The `pandas` functions are used
        internally for delta date calculations.

    """

    def __init__(self, model, decision_date, before_parameter, after_parameter, earliest_date=None, latest_date=None, decision_freq='AS', **kwargs):
        super(TransientDecisionParameter, self).__init__(model, **kwargs)
        self._decision_date = None
        self.decision_date = decision_date

        if not isinstance(before_parameter, Parameter):
            raise ValueError('The `before` value should be a Parameter instance.')
        before_parameter.parents.add(self)
        self.before_parameter = before_parameter

        if not isinstance(after_parameter, Parameter):
            raise ValueError('The `after` value should be a Parameter instance.')
        after_parameter.parents.add(self)
        self.after_parameter = after_parameter

        # These parameters are mostly used if this class is used as variable.
        self._earliest_date = None
        self.earliest_date = earliest_date

        self._latest_date = None
        self.latest_date = latest_date

        self.decision_freq = decision_freq
        self._feasible_dates = None
        self.integer_size = 1  # This parameter has a single integer variable

    def decision_date():
        def fget(self):
            return self._decision_date

        def fset(self, value):
            if isinstance(value, pd.Timestamp):
                self._decision_date = value
            else:
                self._decision_date = pd.to_datetime(value)

        return locals()

    decision_date = property(**decision_date())

    def earliest_date():
        def fget(self):
            if self._earliest_date is not None:
                return self._earliest_date
            else:
                return self.model.timestepper.start

        def fset(self, value):
            if isinstance(value, pd.Timestamp):
                self._earliest_date = value
            else:
                self._earliest_date = pd.to_datetime(value)

        return locals()

    earliest_date = property(**earliest_date())

    def latest_date():
        def fget(self):
            if self._latest_date is not None:
                return self._latest_date
            else:
                return self.model.timestepper.end

        def fset(self, value):
            if isinstance(value, pd.Timestamp):
                self._latest_date = value
            else:
                self._latest_date = pd.to_datetime(value)

        return locals()

    latest_date = property(**latest_date())

    def setup(self):
        super(TransientDecisionParameter, self).setup()

        # Now setup the feasible dates for when this object is used as a variable.
        self._feasible_dates = pd.date_range(self.earliest_date, self.latest_date,
                                                 freq=self.decision_freq)

    def value(self, ts, scenario_index):

        if ts is None:
            v = self.before_parameter.get_value(scenario_index)
        elif ts.datetime >= self.decision_date:
            v = self.after_parameter.get_value(scenario_index)
        else:
            v = self.before_parameter.get_value(scenario_index)
        return v

    def get_integer_lower_bounds(self):
        return np.array([0, ], dtype=np.int)

    def get_integer_upper_bounds(self):
        return np.array([len(self._feasible_dates) - 1, ], dtype=np.int)

    def set_integer_variables(self, values):
        # Update the decision date with the corresponding feasible date
        self.decision_date = self._feasible_dates[values[0]]

    def get_integer_variables(self):
        return np.array([self._feasible_dates.get_loc(self.decision_date), ], dtype=np.int)

    def dump(self):

        data = {
            'earliest_date': self.earliest_date.isoformat(),
            'latest_date': self.latest_date.isoformat(),
            'decision_date': self.decision_date.isoformat(),
            'decision_frequency': self.decision_freq
        }

        return data

    @classmethod
    def load(cls, model, data):

        before_parameter = load_parameter(model, data.pop('before_parameter'))
        after_parameter = load_parameter(model, data.pop('after_parameter'))

        return cls(model, before_parameter=before_parameter, after_parameter=after_parameter, **data)

TransientDecisionParameter.register()

```



Now when running this network in WaterStrategy, a TranscientDecisionParameter will be registered.&#x20;

Make sure after saving your Custom Rule, it is displayed on the left side, in this case under **Parameter** section

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

## Using TranscientDecisionParameter

For this case, we will double the max volume of **New Reservoir** storage node starting on `2045-01-01`

Go to **New Reservoir** storage node and `Edit` **Max Volume**

<figure><img src="../../.gitbook/assets/image (53).png" alt="" width="446"><figcaption></figcaption></figure>

Select in **Options** tab **PYWR\_PARAMETER**

<figure><img src="../../.gitbook/assets/image (54).png" alt="" width="271"><figcaption></figcaption></figure>

Paste the following code and click **Save**

```
{
  	"type": "TransientDecisionParameter",
	"after_parameter": "__New reservoir__:max_volume after",
	"before_parameter": "__New reservoir__:max_volume before",
	"decision_date": "2045-01-01",
	"latest_date": "2045-01-01"
}
```

TranscientDecisionParameter includes attributes `before_parameter` and `after_parameter` which we will have to create as following:



<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

A small text box will open, when we can write the name of our new **PWR\_PARAMETER**, in this case\
\_\_**New reservoir\_\_:max\_volume before.** Click **Enter**.\


<figure><img src="../../.gitbook/assets/image (57).png" alt="" width="375"><figcaption></figcaption></figure>

WaterStrategy will open the parameter window, paste the following code and **Save**

**\_\_New reservoir\_\_:max\_volume before:**

```
{
	"type": "ConstantParameter",
	"value": 120000
}
```

<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

Repeat to create the max volume after parameter

**\_\_New reservoir\_\_:max\_volume after:**

```
{
	"type": "ConstantParameter",
	"value": 240000
}
```



As last step, `TranscientDecisionParameter` needs **Initial Volume Proportion** for the storage node as the parameter inherit initial values from the node, in this case we will setup to **0.99**

<figure><img src="../../.gitbook/assets/image (59).png" alt="" width="423"><figcaption></figcaption></figure>



## Results

As we can see in the following picture, we are combining pywr-scenarios using Climate Change and increasing the volume of our selected reservoir from 120.000 Ml to 240.000 Ml in 1st january 2045.

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption><p>simulated volume (New Reservoir)</p></figcaption></figure>



