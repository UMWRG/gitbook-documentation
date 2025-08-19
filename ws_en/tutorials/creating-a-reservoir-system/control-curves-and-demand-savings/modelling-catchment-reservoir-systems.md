# Adding reservoir control curves and demand savings (reductions)

## Introduction

Control curves can be used to implement a demand reductions when reservoir levels go below certain thresholds. This represents the implementation of temporary demand management measures. In this exercise the demand will be incrementally reduced as the reservoir goes below certain storage thresholds. This exercise will demonstrate the[ Control Curve Index Parameter](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/control-curve-index-parameter), the [Indexd Array Parameter](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/indexed-array-parameter) as well as the [Aggregated Parameter](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/aggregated-parameter) as well as parameter nesting.

## Clone the scenario and define a control curve

1. Clone the **'Balanced sources'** scenario and name the new one **'Demand reductions'**
2. First we will define a **control curve** which uses storage volume thresholds to progressively reduce demand to model demand restrictions being placed on a demand. The first curve is a [Monthly Profile](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/monthly-profile) (60% in come months and 45% in others) allowing for seasonal changes while the two subsequent curves are [Constants ](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/constant)(40% and 10% of reservoir storage capacity).

<figure><img src="../../../.gitbook/assets/image (128).png" alt=""><figcaption><p>Reservoir control curve</p></figcaption></figure>

The Control Curve will be defined in the **Parameters** tab. In the Parameters tab add a **Pywr\_Parameter**.

<figure><img src="../../../.gitbook/assets/image (129).png" alt="" width="375"><figcaption><p>Add a Pywr_Parameter</p></figcaption></figure>

Name the parameter **'storage control curve'** and press _Enter_**.**

<figure><img src="../../../.gitbook/assets/image (131).png" alt="" width="335"><figcaption><p><strong>storage control curve</strong></p></figcaption></figure>

Paste in the following JSON code snippet below. Please note how the `"Example reservoir"` is referenced in the `"storage_node"`attribute.

```
{
	"type": "controlcurveindexparameter",
	"storage_node": "Example reservoir",
	"control_curves": [
		{
			"type": "monthlyprofileparameter",
			"values": [
				0.45,
				0.45,
				0.45,
				0.45,
				0.45,
				0.45,
				0.45,
				0.45,
				0.45,
				0.45,
				0.6,
				0.6
			]
		},
		{
			"type": "constant",
			"value": 0.4
		},
		{
			"type": "constant",
			"value": 0.1
		}
	],
	"__recorder__": {
		"timeseries": true
	}
}
```

<figure><img src="../../../.gitbook/assets/image (132).png" alt=""><figcaption><p>Paste the code and save</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (133).png" alt=""><figcaption><p>Select recording timeseries and save</p></figcaption></figure>

At each time step the [Control Curve Index Parameter](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/control-curve-index-parameter) will return an Index Value as shown below:

<figure><img src="../../../.gitbook/assets/image (134).png" alt=""><figcaption><p>Reservoir control curve</p></figcaption></figure>

These Indices can be associated to a Demand Factor which will be defined using an [Indexed Array Parameter](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/indexed-array-parameter). The Demand factor will be used to reduce demand when each control curve threshold is passed.

## Associate demand factor

1. We will associate the following **Demand Factors** to the different control curve failure levels:

<figure><img src="../../../.gitbook/assets/image (135).png" alt=""><figcaption><p>Reservoir control curve</p></figcaption></figure>

These will reduce demand to 90%, 80% and 50% of the Baseline demand corresponding to 10%, 20% and 50% demand reductions.

2. Create a new **Pywr\_Parameter**

<figure><img src="../../../.gitbook/assets/image (136).png" alt=""><figcaption><p>Create a new Pywr_Parameter</p></figcaption></figure>

3. Name the parameter **'control curve demand factor'** and press _Enter_**.**

<figure><img src="../../../.gitbook/assets/image (137).png" alt="" width="275"><figcaption><p>Name the parameter</p></figcaption></figure>

4. Paste in the following JSON code snippet below. Please note how the`"`storage `control curve"` is referenced in the `"index_parameter"`attribute.

```
{
	"type": "indexedarrayparameter",
	"index_parameter": "storage control curve",
	"params": [
		1,
		0.9,
		0.8,
		0.5
	],
}
```

<figure><img src="../../../.gitbook/assets/image (138).png" alt=""><figcaption><p>Paste the code and save</p></figcaption></figure>

The `Params`attribute takes in either scalars or Pywr parameters and the index of the array corresponds to index in the Parameter referenced in the **index\_parameter** which in this case is the control curve.

5. Select to make this Parameter output.

<figure><img src="../../../.gitbook/assets/image (139).png" alt=""><figcaption><p>Select recording timeseries and save</p></figcaption></figure>

## Define the baseline demand

Next we will define the baseline demand. This is the demand that the reservoir has before any reductions are implemented. In previous tutorial, the Example demand is defined as a scalar (0.1) on the Max\_flow attribute of the Example demand output node:

<figure><img src="../../../.gitbook/assets/image (140).png" alt=""><figcaption><p>Example demand</p></figcaption></figure>

We will replace this with a **Parameter reference.**

1. First, we will define the baseline demand using a **Constant Parameter.**

Add a new **Pywr\_parameter.**

<figure><img src="../../../.gitbook/assets/image (142).png" alt=""><figcaption><p>Add a new Pywr_parameter</p></figcaption></figure>

And name it **Baseline demand** and press _Enter_.

<figure><img src="../../../.gitbook/assets/image (143).png" alt="" width="274"><figcaption><p>Name the new Pywr_parameter</p></figcaption></figure>

2. The baseline demand will remain 0.1 Mm3/day. Copy and paste the JSON code snippet into the JSON tab.

```
{
	"type": "constant",
	"value": 0.1
}
```

<figure><img src="../../../.gitbook/assets/image (144).png" alt=""><figcaption><p>Paste the code and save</p></figcaption></figure>

At each time step, the modeled demand will be the Baseline Demand multiplied by the Demand Factor:

`Timestep demand = Baseline demand x Demand Factor`

## Calculate **timestep demand**

This can be accomplished by using an [Aggregated Parameter](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/aggregated-parameter).

1. Add a new **Pywr\_parameter.**

<figure><img src="../../../.gitbook/assets/image (145).png" alt=""><figcaption><p>Add a new Pywr_parameter</p></figcaption></figure>

Name the new parameter **'timestep demand'**

<figure><img src="../../../.gitbook/assets/image (146).png" alt="" width="274"><figcaption><p>Name the new parameter</p></figcaption></figure>

2. Copy and paste the JSON code snippet into the JSON tab.

```
{
	"type": "AggregatedParameter",
	"agg_func": "product",
	"parameters": [
		"baseline demand",
		"control curve demand factor"
	]
}
```

<figure><img src="../../../.gitbook/assets/image (147).png" alt=""><figcaption><p>Paste the code and save</p></figcaption></figure>

Select to make this Paramter value be output in each time step.

<figure><img src="../../../.gitbook/assets/image (148).png" alt=""><figcaption><p>Select recording the timeserries</p></figcaption></figure>

3. The **'timestep demand'** defines the demand at each time step taking into account the state (i.e. real-time storage) in the Reservoir.

This **Parameter** needs to be referenced on the **max\_flow** attribute of the Demand node.

4. Click on the Demand node and write or paste '**timestep demand'** in the max\_flow attribute replacing the scalar value (0.1).

<figure><img src="../../../.gitbook/assets/image (155).png" alt=""><figcaption><p>Enter max_flow attribute name</p></figcaption></figure>

Please note, if the Parameter name does not save, change the type of the entry to **"Descriptor"**.

<figure><img src="../../../.gitbook/assets/image (156).png" alt=""><figcaption><p>Click on edit the max_flow</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (151).png" alt=""><figcaption><p>Select DESCRIPTOR</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (157).png" alt=""><figcaption><p>Enter the name</p></figcaption></figure>

Don't forget to save the changes.

## Run the model and view the results

1. **Run** the model.

<figure><img src="../../../.gitbook/assets/image (161).png" alt="" width="327"><figcaption><p>Click on to run the model</p></figcaption></figure>

2. View the **simulated** \_volume on the Reservoir

<figure><img src="../../../.gitbook/assets/image (153).png" alt=""><figcaption><p>Simulated _volume on the Reservoir</p></figcaption></figure>

You can **zoom** into the drought, for example this is the drought that occurred in 2042-2044.

<figure><img src="../../../.gitbook/assets/image (154).png" alt=""><figcaption><p>Simulated _volume on the Reservoir in 2042-2044</p></figcaption></figure>

In the the Scenario with demand reductions, the Reservoir did not go to as low of storage (9.4 vs 8.17 Mm3).

3. Click on the simulated\_flow of the Demand node. The demand reductions can be seen.

<figure><img src="../../../.gitbook/assets/image (158).png" alt=""><figcaption><p>simulated_flow of the Demand node</p></figcaption></figure>

4. You can view the control cure parameter output by clicking on the **Network Data** view.

<figure><img src="../../../.gitbook/assets/image (159).png" alt=""><figcaption><p>Click to view the control cure parameter output</p></figcaption></figure>

Clicking on **simulated\_storage control curve** shows what index the storage control curve is returning at each time step. This varies between 0-2.

<figure><img src="../../../.gitbook/assets/image (160).png" alt=""><figcaption><p>Control cure parameter output</p></figcaption></figure>

## Exercise <a href="#exercise" id="exercise"></a>

1. Increase the Baseline Demand Parameter. How high can baseline demand be before the reservoir fully empties?
