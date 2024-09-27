# Add Data to the Nodes

Please use the data in the online Excel table below for this tutorial.

[https://docs.google.com/spreadsheets/d/1J\_wU\_-U\_ZlOLdbmg7rgW1HMt14JfHQHS/edit?usp=sharing\&ouid=103412600775811717846\&rtpof=true\&sd=true](https://docs.google.com/spreadsheets/d/1J\_wU\_-U\_ZlOLdbmg7rgW1HMt14JfHQHS/edit?usp=sharing\&ouid=103412600775811717846\&rtpof=true\&sd=true)&#x20;

Please watch this video for more detail. The data in the video may look different to the data provided in the Excel.

{% embed url="https://youtu.be/I0SZ9GXLmXk" %}

We want to include **time series** for the flow in the catchment node and **scalar** values for Demand.

1. Double click on demand and update the attributes in the Inputs section as shown below:

Max\_flow = 0

Allocation penalty = 0

You may need to click on the edit ![](<../../.gitbook/assets/0 (11).png>) button to change the values.

![](<../../.gitbook/assets/1 (11).png>)

1. Double click on catchment node, on the right panel inside Inputs section, on **flow** attribute click on the edit button ![](<../../.gitbook/assets/2 (10).png>).

![](<../../.gitbook/assets/3 (10).png>)

new window will appear, Click **Options**, select **PYWR\_DATAFRAME** and click **Save**

![](<../../.gitbook/assets/4 (10).png>)

1. The window will update to the Dataframe tab. Copy the data from the Excel file using the link above and paste it as shown in the image. Note that 2 columns must be used, column A for the date-time index and column B for the data values. Click **Save. For more detail please watch the video.**

<figure><img src="../../.gitbook/assets/Screen Shot 2024-08-08 at 12.56.21 AM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screen Shot 2024-08-08 at 12.57.23 AM.png" alt=""><figcaption></figcaption></figure>
