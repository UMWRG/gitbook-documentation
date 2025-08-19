# Adding a Source Representing Groundwater

In this section an [Input ](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/node-types/input-node)node representing a groundwater source will be added to the reservoir system. The demand node will receive water from both groundwater and the reservoir. Groundwater is modeled as a yield.

## Create a new scenario

Clone the **'Demand with treatment losses'** scenario and call the new one **'Demand with GW'**

## **Add an input node**

Add an **Input** node below the demand node as shown below. Rename the node to 'Groundwater well'

<figure><img src="../../.gitbook/assets/image (235).png" alt=""><figcaption><p>Add groundwater input</p></figcaption></figure>

**###Notice**: to maintain the same behaivior in each of the previous scenarios, the Max Fow of the input node must be set to 0 in each scenario.&#x20;

This can be done by clicking on the edit button on the Max Flow attribute of the Input node.

<figure><img src="../../.gitbook/assets/image (236).png" alt="" width="367"><figcaption><p>Edit the max flow</p></figcaption></figure>

and then by setting a Max Flow of 0 Mm3/day in the text box:

<figure><img src="../../.gitbook/assets/image (237).png" alt="" width="226"><figcaption><p>Set max flow to 0</p></figcaption></figure>

and before saving the changes, select all scenarios so the 0 flow applies to all scenarios:

<figure><img src="../../.gitbook/assets/image (238).png" alt=""><figcaption><p>Select all scenarios</p></figcaption></figure>

and then click on **save**.

## Groundwater inflow setting

Next, we need to set the yield of the groundwater in this scenario. Set the **Max Flow** of the node to be **0.02 Mm3/day** instead of 0**.** This will represent the maximum possible supply of the input node at each time step.

<figure><img src="../../.gitbook/assets/image (239).png" alt=""><figcaption><p>Groundwater input</p></figcaption></figure>

Then, run this scenario.

<figure><img src="../../.gitbook/assets/image (240).png" alt="" width="267"><figcaption><p>Run the scenario</p></figcaption></figure>

## View and compare the results

Compare the **simulated\_volume** of the reservoir to that of the **'Demand with treatment losses'** scenario.

<figure><img src="../../.gitbook/assets/image (241).png" alt="" width="363"><figcaption><p>Select the scenario to compare</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (242).png" alt=""><figcaption><p>Compare the reservoir volume</p></figcaption></figure>

## Exercises and questions <a href="#exercises-and-questions" id="exercises-and-questions"></a>
