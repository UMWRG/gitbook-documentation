---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Adding reservoir bathymetry (Area)

## Background <a href="#background" id="background"></a>

The Area that a Reservoir or Storage node covers depends on how full the reservoir is.

The **Area Rating Curve** <mark style="color:purple;">determines gives</mark> the Area of a reservoir as a function of its Level or Storage. In WaterStrategy and Pywr, the time step storage of a reservoir is known at each time step. We can use this storage with an Area rating cure to calculate the reservoir area and therefore its evaporation at each time-step.

Below is an example Area rating table:

| Volume (Mm3) | Area (Km2) |
| ------------ | ---------- |
| 0            | 1          |
| 7            | 2          |
| 10           | 4          |
| 15           | 6          |
| 25           | 14         |

When plotted it looks like this:

<figure><img src="../../../.gitbook/assets/image (162).png" alt=""><figcaption><p>Area Rating Curve</p></figcaption></figure>

[Pywr Parameters ](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters)are functions that return a value in the model at each time-step. These values can be a constant, based on time (e.g. on the day or month), a calculation based on the time step reservoir storage and many other calculations. In this case, we are interested in a parameter that returns the Area of a reservoir or storage node as a function of its time-step storage. To do this we use an [Interpolated Volume Parameter](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/interpolated-volume).

The interpolated volume parameter uses an **array** (table) of **Reservoir Volumes** and corresponding values. In this case the associated values are the corresponding **Reservoir Area** for a given **Volume**. In between the given points in the table, the parameter interpolates.

_**Please note:** Parameters can be defined directly on a node or they can be defined in the Parameters tab in the interface. Parameters that are defined in the Parameters tab in the interface can be used on multiple nodes and nested within different parameters._

_This tutorial includes both types of definitions. The area will be defined on the node, while the level parameter (next step) will be defined in the Parameters tab._

## Tutorial <a href="#tutorial" id="tutorial"></a>

1. Clone the **'Demand with treatment losses'** scenario and call the new one **'Adding reservoir P and E'.** The P stands for Precipitation and E stands for Evaporation.&#x20;
2. Click on the **Reservoir** and edit the **Area** attribute.

<figure><img src="../../../.gitbook/assets/image (115).png" alt="" width="375"><figcaption><p>Edit the Area attribute</p></figcaption></figure>

3. The Interpolated Volume Parameter does not currently have a JSON editor in WaterStrategy. In order to define this parameter on this attribute, we need to use the generic **PYWR\_PARAMETER**. This allows us to put in the JSON for any Pywr parameter.

<figure><img src="../../../.gitbook/assets/image (85).png" alt="" width="375"><figcaption><p>Selecy PYWR_PARAMETER</p></figcaption></figure>

Press **OK**

<figure><img src="../../../.gitbook/assets/image (65).png" alt="" width="315"><figcaption><p>Allow the change</p></figcaption></figure>

\
4\. Copy and Paste the JSON code below into the text in the **JSON tab**

<figure><img src="../../../.gitbook/assets/image (84).png" alt=""><figcaption><p>Paste the JSON code and save</p></figcaption></figure>

```
{
	"type": "InterpolatedVolumeParameter",
	"node": "Example reservoir",
	"volumes": [
		0,
		7,
		10,
		15,
		25
	],
	"values": [
		1,
		2,
		4,
		6,
		14
	],
	"interp_kwargs": {
		"kind": "linear"
	},
	"comment": "volumes: Mm3, values:  Km2"
}
```

5. You can select to record the parameter value as a time series by selecting **Timeseries** in the **Outputs** tab. Then, save it.

<figure><img src="../../../.gitbook/assets/image (86).png" alt=""><figcaption><p>Select to record the parameter and save</p></figcaption></figure>

6. Run the model and view the **Simulated\_Area** output

<figure><img src="../../../.gitbook/assets/image (68).png" alt=""><figcaption><p>Simulated_Area output</p></figcaption></figure>

This shows the Area of the reservoir over time.

<figure><img src="../../../.gitbook/assets/image (88).png" alt=""><figcaption><p>Area of the reservoir</p></figcaption></figure>

Smaller areas correspond with lower reservoir storage volumes.
