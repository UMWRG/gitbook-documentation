# Reading h5 DataFrame for pywr-scenarios

Go to the catchment node **Days Weir,** click Edit **Flow**

<figure><img src="../../.gitbook/assets/image (42).png" alt="" width="563"><figcaption></figcaption></figure>

A new window will pop up, select **PYWR\_PARAMETER** and click **Save**

<figure><img src="../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>



Paste the following configuration and **Save**

```json
{
	"key": "Days Weir",
	"scenario": "Climate Change",
	"type": "DataFrameParameter",
	"url": "Thames_inflows_pywrScenarios.h5",
	"index_col": "timestep",
	"parse_dates": true
}
```

It should look like the following image

<figure><img src="../../.gitbook/assets/image (44).png" alt="" width="563"><figcaption></figcaption></figure>

Repeat the procedure for catchment **Lower\_Thames** using the following configuration

```json
{
	"key": "Lower Thames",
	"scenario": "Climate Change",
	"type": "DataFrameParameter",
	"url": "Thames_inflows_pywrScenarios.h5",
	"index_col": "timestep",
	"parse_dates": true
}
```

## Results

As the total number of simulations is four, this is because we are using a single **pywr-scenarios** setup for **Climate Change**, which contains 4 scenarios. Each of these scenarios will run separately, and the result of all 4 simulations will be displayed each output result, as shown below

<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption><p>simulated_flow (Lower_Thames)</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (48).png" alt=""><figcaption><p>simulated_volume (New Reservoir)</p></figcaption></figure>

