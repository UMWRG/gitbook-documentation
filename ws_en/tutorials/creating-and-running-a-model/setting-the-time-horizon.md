# Setting the Time Horizon

Please watch the video page for more detail.

{% embed url="https://youtu.be/I0SZ9GXLmXk?t=165" %}

Click on the the **network level data** menu button.

<figure><img src="../../.gitbook/assets/image (20) (1).png" alt=""><figcaption></figcaption></figure>

The network level data window appears.&#x20;

The **timestepper.start, timestepper.end** and **timestepper.timestep** settings need to be defined which are the start and end dates of the models time horizon and the time step at which the model will be run.&#x20;

The time series in our data set is monthly however we will run the model at a 1 Day time step (1D). Time steps can be in any number of days, weekly (W) and monthly (M).

Please set the data as follows:

&#x20;**timestepper.end** = 2021-12-01

&#x20;**timestepper.start =** 2020-01-01

**timestepper.timestep =** D



Click the **Edit** button, select **Descriptor** for each of the time step attributes.&#x20;

Input the following data above and click **Save**.

This time horizon can be shorter than our input data, but the start and end dates must be within the range of your data. The date format and syntax is strict.

<figure><img src="../../.gitbook/assets/Screen Shot 2024-08-08 at 1.03.19 AM.png" alt=""><figcaption></figcaption></figure>
