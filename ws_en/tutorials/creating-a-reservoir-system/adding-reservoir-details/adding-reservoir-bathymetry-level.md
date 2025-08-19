# Adding reservoir bathymetry (Level)

The water **Level** of a reservoir can be calculatedi n the same way as for a reservoir. A reservoir's water level is required to be able to calculate hydropower. While the Botswana National Model doesn't include hydropower, for completeness it is included in this tutorial.

_Please note: Unlike the Area parameter that was defined on the Resevoir node. We will define the Level parameter in the Parameters tab of the Interface. This is to demonstrate the Parameters tab, the Level could be defined also on the node._

Below is an example area Level vs Volume rating table for:

| Volume (Mm3) | Level (m) |
| ------------ | --------- |
| 0            | 1         |
| 7            | 8         |
| 10           | 16        |
| 15           | 18        |
| 25           | 20        |

When plotted it looks like this:

<figure><img src="../../../.gitbook/assets/image (70).png" alt=""><figcaption><p>Relationship between the water level and the reservoir volume</p></figcaption></figure>

1. Click on the **Parameters** tab on the interface.

<figure><img src="../../../.gitbook/assets/image (116).png" alt=""><figcaption><p>Click on the Parameters tab</p></figcaption></figure>

2. Click on the **+** to add a new parameter. Select **PYWR\_PARAMETER**

<figure><img src="../../../.gitbook/assets/image (77).png" alt=""><figcaption><p>Select PYWR_PARAMETER</p></figcaption></figure>

3. In the text field that appears write **'Dam level'**

<figure><img src="../../../.gitbook/assets/image (73).png" alt="" width="375"><figcaption><p>Name the parameter</p></figcaption></figure>

4. Copy and **Paste** the Json below into the editor and click **Save**.

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
		8,
		16,
		18,
		20
	],
	"interp_kwargs": {
		"kind": "linear"
	},
	"comment": "volumes: Mm3, values: m"
}
```

<figure><img src="../../../.gitbook/assets/image (93).png" alt=""><figcaption><p>Paste the code and save</p></figcaption></figure>

5. Click on **Timeseries** in the **Outputs** tab to enable the saving of the Level timeseries.

<figure><img src="../../../.gitbook/assets/image (94).png" alt=""><figcaption><p>Enable the saving of the Level timeseries</p></figcaption></figure>

6. Click on **Map** to return to the map view

<figure><img src="../../../.gitbook/assets/image (95).png" alt=""><figcaption><p>Return to the map view</p></figcaption></figure>

\
7\.   The Dam level parameter needs to be referenced on the Level attribute on the reservoir, to do this, click on the Reservoir an write the name of the parameter in the Level attribute (**Dam level).** Please note that the name is case sensitive.

<figure><img src="../../../.gitbook/assets/image (121).png" alt=""><figcaption><p>Enter the parameter's name</p></figcaption></figure>

8. Run the model.
9. You will see that because the **Dam level** parameter is not defined on the node, the **simulated\_level** is not output on the reservoir node. Instead to view the output, click on the **Network Attributes** button.

<figure><img src="../../../.gitbook/assets/image (82).png" alt="" width="288"><figcaption><p>Click on the Network Attributes button</p></figcaption></figure>

10. Click on the **simulated\_Dam level.** Note that the Reservoir node name is in the name of the output of the Parameter.

<figure><img src="../../../.gitbook/assets/image (98).png" alt="" width="348"><figcaption><p>View the Dam level</p></figcaption></figure>

**The Level time series can be seen below.**

<figure><img src="../../../.gitbook/assets/image (120).png" alt=""><figcaption><p>Level time series</p></figcaption></figure>
