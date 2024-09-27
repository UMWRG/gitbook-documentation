# Adding a Reservoir

Please watch the video to add a reservoir node to the model built in the previous tutorial. To do this, please create a copy of the model as shown in the video and please work in the **With abstraction** scenario

{% embed url="https://www.youtube.com/watch?v=XjGGR3ISefU" %}

Drag and drop a **Storage** ![](<../../.gitbook/assets/image (3).png>) node on the network. Then delete the link conecting the **Catchment** node to the **Link** node. Connect the **Catchment** node to the **Storage** node and then connect the **Storage** node to the **Link** node.

Initially set the the **max\_volume** of the storage node to 0 Mm3 and the **initial\_volume\_pc** to 0 and run the model.

Then clone the **With\_abstraction** scenario and make a new scenario called **'Reservoir with storage and abstraction'.**

In the new scenario, set the **max\_volume** of the storage node to 6 Mm3 and the **initial\_volume\_pc** to 0.33. The reservoir will then begin the simulation at 30% full. Alternatively the **initial\_volume** can be set at 1.8 Mm3. Either **initial\_volume**  or **initial\_volume\_pc** needs to be set.

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

Run the model and view the **simulated\_volume** of the reservoir.

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

The resrevoir empties every dry season and fills every wet season.&#x20;

Compare the **simulated\_flow** on the demand node for the **'Reservoir with storage and abstraction'** and **'With abstraction'** scenario**.**

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

The storage reduced the deficit in the demand node. However, we can see that even with the storage, there are times that the demand node does not receive its full demand of 0.7 Mm3.

## Exercise

We saw that under flow Scenario 1, the reservoir would empty every year. How low must the demand be for the reservoir to still have some storage volume even in the dry season?
