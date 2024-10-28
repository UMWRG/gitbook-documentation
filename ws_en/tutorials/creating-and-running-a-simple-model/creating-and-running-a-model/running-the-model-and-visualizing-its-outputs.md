# Running the Model and Visualizing its Outputs

Please watch the video for more details.

{% embed url="https://youtu.be/I0SZ9GXLmXk?t=289" %}

Click the **Run a Model** icon ![](<../../../.gitbook/assets/image (12) (1).png>), select **Run Pywr** and click **Submit**.

<figure><img src="../../../.gitbook/assets/image (13) (1).png" alt=""><figcaption></figcaption></figure>

The model will be submitted to run on the cloud.

You will see the Run appear in the Runs menu.

A blue ribbon means the run is running.

<figure><img src="../../../.gitbook/assets/image (14) (1).png" alt=""><figcaption></figcaption></figure>

A yellow ribbon means the run is queing

<figure><img src="../../../.gitbook/assets/image (19) (1).png" alt=""><figcaption></figcaption></figure>

A green ribbon means the run has finished successfully

<figure><img src="../../../.gitbook/assets/image (15) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;A red ribbon means the run has termined with an error.

<figure><img src="../../../.gitbook/assets/image (16) (1).png" alt=""><figcaption></figcaption></figure>



Clicking on the ribbon opens a window with the run log. If there is an error, a traceback will appear at the bottom and can be used to help identify why the run had an error.

<figure><img src="../../../.gitbook/assets/image (18) (1).png" alt=""><figcaption></figcaption></figure>



Once the model has sucessfully ran, you can click on the various nodes to examine their time series output. In this case, the main output attribute is the 'simulated flow'.&#x20;

Double click on the node of interest. “Simulated\_flow” will be available under the Output Section, click on the edit button ![](<../../../.gitbook/assets/image (26) (1).png>)to see results. Click on the Demand node which is the node on the right.

<figure><img src="../../../.gitbook/assets/image (25) (1).png" alt=""><figcaption></figcaption></figure>

A time series table first appears:

<figure><img src="../../../.gitbook/assets/Screen Shot 2024-08-08 at 1.08.21 AM.png" alt=""><figcaption></figcaption></figure>

Click on **Plot** to see a plot of the time series.

<figure><img src="../../../.gitbook/assets/Screen Shot 2024-08-08 at 1.08.29 AM.png" alt=""><figcaption></figcaption></figure>

As the max\_flow of the demand node was set to 0, there is no flow in this node.

On the next flow, we will create a new scenario and change the max\_flow of the demand node.

What is the simulated flow on the downstream output node representing the river outlet?

<figure><img src="../../../.gitbook/assets/Screen Shot 2024-08-08 at 1.10.34 AM.png" alt=""><figcaption></figcaption></figure>
