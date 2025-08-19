# Adding a Water Treatment Works with Losses

In this section a [**loss link**](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/node-types/loss-link-node) representing a **potable water treatment works** will be added to the system. This node is used to represent treatment **losses** leaving the system. Water from the reservoir is released to the water treatment works where, a proportion of this water is lost via process losses and the remaining water is then supplied to the demand.

## Create a new senario

* Clone the **'With demand'** scenario and call the new one **'Demand with treatment losses'.**
* Delete the link connecting the reservoir to the Example demand node by **right** clicking on the link and clicking on **'Delete Link'**

<figure><img src="../../.gitbook/assets/image (226).png" alt="" width="364"><figcaption><p>Delete the link</p></figcaption></figure>

## Add a loss link

* Place a loss link <img src="../../.gitbook/assets/image (227).png" alt="" data-size="line">in between the reservoir and the demand and connect the reservoir to the losslink and losslink to the demand node with links. Rename the loss link to be **'Water Treatment Works'.**

<figure><img src="../../.gitbook/assets/image (228).png" alt=""><figcaption><p>Place a loss link</p></figcaption></figure>

* This water treatment works will have 10% losses based on the outflow of the water treatment works.
* Set the **Loss Factor** to be 0.1 representing 10% losses.
* Set the Loss Factor Type to be **net** so that the 10% loss is calculated to the output of the treatment works.

<figure><img src="../../.gitbook/assets/image (231).png" alt=""><figcaption><p>Loss node setting</p></figcaption></figure>

## Run the scenario

<figure><img src="../../.gitbook/assets/image (232).png" alt="" width="265"><figcaption><p>Run the model</p></figcaption></figure>

## View and compare the results

Compare the **simulated\_volume** of the reservoir in the **'Baseline'** and the **'With demand'** scenario.

<figure><img src="../../.gitbook/assets/image (233).png" alt="" width="375"><figcaption><p>Select scenarios to compare</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (234).png" alt=""><figcaption><p>Compare different scenarios</p></figcaption></figure>

The reservoir in the scenario that has treatment losses goes to lower storage during dry periods. This is because the reservoir is release more water to the demand due to the treatment losses.

Has the demand been affected by the treatment losses? Compare the **simulated\_flow** of the Example demand node under this and the **With demand** scenario.

## Exercises and questions <a href="#exercises-and-questions" id="exercises-and-questions"></a>

1. The water treatment works results in losses leaving the system. The simulated flow of the loss link shows the flow output of the loss link. **How can we determine how much water is entering the water treatment works?**

&#x20;       _Hint: Place a normal link node in-between the reservoir and loss link and rerun the model. The simulated flow on this node will represented the flow released by the reservoir and the flow going into the treatment works before losses._

1. **In an new scenario, increase the net losses to 20%? How does this affect the reservoir simulated volume?**
