# Reading CSV DataFrame

Go to **New Reservoir Release** node and change **Max Flow** to **-400**, this will allow to flow water through this node

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>



The downloaded file, **Thames\_Lee\_Valley\_demand.csv**, contains a time series dataset structured with two key columns:

**timestep:** This column will serve as the index for the time series. It represents the progression of time in the dataset, allowing for chronological organization.

**Lee Valley Demand:** This column contains the data representing demand values in the Lee Valley.&#x20;



<figure><img src="../../.gitbook/assets/image (3).png" alt="" width="443"><figcaption><p><strong>Thames_Lee_Valley_demand</strong></p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Select the output node **Lee Valley Demand** and Edit the **Max Flow**

<figure><img src="../../.gitbook/assets/image (5).png" alt="" width="563"><figcaption></figcaption></figure>

In Options select **PYWR\_PARAMETER**

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Paste the following configuration:

```json
{
	"type": "DataFrameParameter",
	"url": "Thames_Lee_Valley_demand.csv",
	"column": "Lee Valley Demand",
	"index_col": "timestep",
	"parse_dates": true
}
```

Now it should look as the following image:

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

### Results

Click on node Lee Valley Demand > Outputs > simulated\_flow to see results of the simulation

<figure><img src="../../.gitbook/assets/image (38).png" alt="" width="475"><figcaption></figcaption></figure>



<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption><p>simulated_flow (Lee Valley Demand)</p></figcaption></figure>



Now check the **simulated\_volume** for **New reservoir**

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption><p>simulated volume (New Reservoir)</p></figcaption></figure>
