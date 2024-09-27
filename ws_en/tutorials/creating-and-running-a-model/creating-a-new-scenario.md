# Creating a New Scenario

Please watch the video for additional detail.

{% embed url="https://youtu.be/I0SZ9GXLmXk?t=336" %}

### Create new scenario and compare with Baseline

Scenarios allow users to explore and evaluate different conditions or management strategies within the water system model.&#x20;

1\. To create a new scenario, click on the **Clone a scenario** icon.

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

&#x20;choose **Baseline** as the scenario to clone, add a name to your scenario, in this case 'With abstraction', and click **Clone**.

<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

You will see the new scenario is automatically made active.

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

At the moment, the new scenario is an exact clone of the **baseline** scenario.

In this scenario, we will assign a demand to the demand node. Change the max\_flow of the demand output node to 5.0 Mm3/day

<figure><img src="../../.gitbook/assets/Screen Shot 2024-08-08 at 1.13.43 AM.png" alt=""><figcaption></figcaption></figure>

**Run** the new scenario and then view the **simulated\_flow** of the demand node.

<figure><img src="../../.gitbook/assets/Screen Shot 2024-08-08 at 1.17.58 AM.png" alt=""><figcaption></figcaption></figure>

Now the amount of water supplied is no longer 0. The demand attempts to abstract 5.0 Mm3/day of water. However when there is not enough water in the river the full 5.0 Mm3/day cannot be abstracted.

Lets view the simulated\_flow of the sink output node.

<figure><img src="../../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screen Shot 2024-08-08 at 1.18.53 AM.png" alt=""><figcaption></figcaption></figure>

Lets compare the river outflow in both scenarios.

Add the baseline scenario to the view by selecting it in the menu and then pressing the Play  ![](<../../.gitbook/assets/image (43).png>)button

<figure><img src="../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screen Shot 2024-08-08 at 1.20.01 AM.png" alt=""><figcaption></figcaption></figure>

We can see that the less water reaches the outlet in the **With abstraction** scenario and sometimes there is no water flowing into the outlet.
