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

# Additional exercises using allocation penalties and control rules

## Using allocation penalties to balance source <a href="#using-allocation-penalties-to-balance-source-use-in-the-mosetse-system" id="using-allocation-penalties-to-balance-source-use-in-the-mosetse-system"></a>

Allocation penalties can be used to balance the use of sources for demands. In the previous exercises the **Example reservoir** had a static Allocation Penalty of -200.

Parameters can be used to make this Allocation Penalty vary based on real-time storage of the reservoir. This can be done with an **Interpolated Volume Parameter.** Once the Allocation Penalty of the reservoir is made dynamic, it can be used with the allocation penalties of other sources to balance source use.

1. Clone the **'Adding reservoir P and E'** scenario and name the new one **'Balanced sources'**
2. Edit the 'Allocation Penalty' attribute ('cost' attribute) of the Reservoir node and change its type to **'PYWR\_PARAMETER'**

<figure><img src="../../.gitbook/assets/image (109).png" alt=""><figcaption><p>Edit 'cost' attribute ('Allocation Penalty' attribute)</p></figcaption></figure>

3. In the JSON tab paste the following JSON code. This Interpolated Volume Parameter assigns a 0 Allocation Penalty to the reservoir when it is full, and a -200 Allocation penalty when it is empty. When the reservoir is between full and empty, the Allocation Penalty is interpolated between 0 and -200.

```
{
	"type": "InterpolatedVolumeParameter",
	"node": "Example reservoir",
	"volumes": [
		0,
		25
	],
	"values": [
		-200,
		0
	],
	"interp_kwargs": {
		"kind": "linear"
	},
	"comment": "volumes: Mm3, values:  allocation penalty"
}
```

4. On the Groundwater Input node, set the **max\_flow** to 0.02 and set the **allocation penalty** to 50.0. A positive allocation penalty of 50, makes it so the groundwater node is only used when the reservoir has an allocation penalty of less than -50, which is when it is 75% full. This means when the Reservoir is almost full, groundwater will not be used. Only once the reservoir draws down sufficiently, will the groundwater node begin to supply water to the demand.

<figure><img src="../../.gitbook/assets/image (113).png" alt=""><figcaption><p>Set the allocation penalty/cost</p></figcaption></figure>

5. Run the model and view the **simulated\_flow** of the groundwater input node and compare to the **Demand with GW;** and the **simulated\_volume** of the Reservoir node and compare both to the **Adding reservoir P and E**.

<figure><img src="../../.gitbook/assets/image (122).png" alt=""><figcaption><p>Groundwater input comparison</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (114).png" alt=""><figcaption><p>Reservoir volume comparison</p></figcaption></figure>

As you can see the **Balanced scenario** which is **orange**, uses the Groundwater source less than the previous scenario. If the groundwater node has a limited licence, this is a way to preserve the licence volume. This will be shown in another tutorial.

_Hint: You can see the simulated allocation penalty is you tick the time-series output of the Allocation Penalty Pywr\_Parameter. At the moment the simulated penalty is called **simulated\_cost** on the reservoir_

<figure><img src="../../.gitbook/assets/image (124).png" alt=""><figcaption><p>Edit the cost parameter</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (125).png" alt=""><figcaption><p>Choose the timeseries recorder and save</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (126).png" alt=""><figcaption><p>View the cost vary with time</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (123).png" alt=""><figcaption><p>Cost vary with time</p></figcaption></figure>
