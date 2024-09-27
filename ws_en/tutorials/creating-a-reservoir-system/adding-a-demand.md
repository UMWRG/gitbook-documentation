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

# Adding a Demand

In this section an output node representing a municipal demand will be added to the system which will draw water from the reservoir.

## Adding an output node

Add an **output** node to the system which will represent an urban demand that wil abstract water from the reservoir. Rename the node to 'Example demand'.

<figure><img src="../../.gitbook/assets/image (218).png" alt=""><figcaption><p>Adding an output node as a demand</p></figcaption></figure>

## Baseline demand

In the **Baseline** scenario set the following attributes on the **Example demand** node:

<figure><img src="../../.gitbook/assets/image (220).png" alt="" width="375"><figcaption><p>Baseline scenario</p></figcaption></figure>

* **max\_flow** = 0. This represents a deamnd of 0 Mm3/day.
* **allocation\_penalty** = -1000. This represents a high priority for water allocation

<figure><img src="../../.gitbook/assets/image (221).png" alt=""><figcaption><p>The attributes defined on the Example demand node</p></figcaption></figure>

## **Create a new scenariao**

**Create a new scenario called 'With demand'.** For a reminder on how to create a scenario please follow the link below.

{% embed url="https://water-strategy.gitbook.io/water-strategy/tutorials/creating-and-running-a-network/creating-a-new-scenario" %}

## Demand in the new scenario

In the **'With demand'** scenario, set the **max\_flow** of the Example demand to 0.1 Mm3/day and run this scenario ![](https://water-strategy.gitbook.io/\~gitbook/image?url=https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2FLG7JgbktYGchOfcaz0zv%2Fblobs%2FxccVMlqqFMkgoP5T8BDH%2Fimage.png\&width=300\&dpr=4\&quality=100\&sign=530a8e5b\&sv=1).

<figure><img src="../../.gitbook/assets/image (222).png" alt="" width="289"><figcaption><p>Example demand</p></figcaption></figure>

## View and compare the reservoir volume

View the **simulated\_volume** of the reservoir in this scenario and compare against the baseline.

<figure><img src="../../.gitbook/assets/image (223).png" alt="" width="375"><figcaption><p>Selecting baseline to compare</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (224).png" alt=""><figcaption><p>Reservoir volume comparison</p></figcaption></figure>

## Exercises and questions <a href="#exercises-and-questions" id="exercises-and-questions"></a>

In this case, we are modelling the 'live' storage of the reservoir. When the reservoir goes to 0 storage in the model there is still dead storage in the system. At the dead storage level, the remaining water isn't able to be released.

* **How high can the demand go before the reservoir empties to its dead storage?**&#x20;

&#x20;      _To do this, create a new scenario and change the max\_flow of the demand node and rerun the model multiple times until the reservoir reaches 0 storage._

* **What is the maximum monthly spill from the reservoir in the simulation?**&#x20;

&#x20;       _Hint: Look at the simulated\_flow on the spill link node._

* **Create a 'Monthly demand' scenario. Use the following video to help you implement a monthly profile demand, where the Example demand changes based on the months:**&#x20;

&#x20;       Jan-Mar: 0.1 Mm3/day&#x20;

&#x20;       April-June: 0.06 Mm3/day&#x20;

&#x20;       July-Sept: 0.07 Mm3/day&#x20;

&#x20;       Sept-Dec: 0.09 MM3/day

{% embed url="https://www.youtube.com/watch?t=76s&v=DH3z2yQVL6I" %}
