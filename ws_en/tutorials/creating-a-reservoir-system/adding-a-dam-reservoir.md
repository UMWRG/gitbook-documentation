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

# Adding a Dam (Reservoir)

## 1. Difference between storage and reservoir nodes

Please note that there are two nodes in WaterStrategy and Pywr that represent reservoirs. The first is a [**storage** ](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/node-types/storage-node)node and the second is a [**reservoir** ](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/node-types/reservoir-node)node.

Both nodes store water. The reservoir node works just like a storage node, however it has built-in parameters allowing _**evaporation**_ and _**precipitation**_ to be directly represented on the node. To represent _**evaporation**_ and _**precipitation**_ with a storage node, a catchment node connected to the storage node is used to represent precipitation and output node drawing water from the storage node is is used to represent evaporation.

This tutorial will use reservoir nodes to build the reservoir system model.

## 2. Build the example reservoir system model

### **2.1   Click the network created in last section and open it**

<figure><img src="../../.gitbook/assets/image (174).png" alt=""><figcaption><p>Open the created network</p></figcaption></figure>

### **2.2   Find a river on the map**

This tutorial has a recommended location, but it doesn't matter if you cannot find the exact location, just find another location with a river.

<figure><img src="../../.gitbook/assets/image (175).png" alt=""><figcaption><p>Recommended location for this example</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (177).png" alt=""><figcaption><p>The river used in this example</p></figcaption></figure>

### **2.3   Add the following nodes to the network**

* Place a **reservoir** node to the river.

<figure><img src="../../.gitbook/assets/image (179).png" alt="" width="329"><figcaption><p>Reservoir node</p></figcaption></figure>

**###Notice**: make sure you use the 'Reservoir' node: <img src="../../.gitbook/assets/image (180).png" alt="" data-size="line">and not the 'Storage' node: <img src="../../.gitbook/assets/image (181).png" alt="" data-size="line">.

<figure><img src="../../.gitbook/assets/image (192).png" alt=""><figcaption><p>Adding a reservoir node</p></figcaption></figure>

* Place a [**catchment** ](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/node-types/catchment-node)node <img src="../../.gitbook/assets/image (184).png" alt="" data-size="line"> upstream of the reservoir. The catchment node represents the river flowing into the reservoir.

<figure><img src="../../.gitbook/assets/image (193).png" alt=""><figcaption><p>Adding a catchment node</p></figcaption></figure>

* Place an [**output** ](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/node-types/output-node)node <img src="../../.gitbook/assets/image (186).png" alt="" data-size="line">downstream of the reservoir. The output node in this case represents the river outlet.

<figure><img src="../../.gitbook/assets/image (195).png" alt=""><figcaption><p>Adding an output node</p></figcaption></figure>

* Place two [**link** ](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/node-types/link-node)nodes <img src="../../.gitbook/assets/image (189).png" alt="" data-size="line">between the reservoir and output nodes (as shown below). In this case, these link nodes represent the (1) reservoir releases and (2) spill.&#x20;

<figure><img src="../../.gitbook/assets/image (196).png" alt=""><figcaption><p>Adding link nodes</p></figcaption></figure>

The **upper link node** representing the reservoir release represents flow that leaves the reservoir as a result of any release rules or to meet downstream allocations. Release rules would generally be specified on this node. Reservoir release rules defined on this node are usually represented by a parameter defined on the nodes max\_flow attribute.

The **lower link node** represents the spill from the reservoir. The spill is used if reservoir release rules are defined constraining how much water can be released via this node and additional water needs to be released than is allowed by the release rules (for example if the reservoir is over capacity). As the spill is generally used only when the reservoir is over capacity, this node generally has a highly positive allocation penalty.

Connect the nodes with edges which are commonly referred to _links_. <img src="../../.gitbook/assets/image (191).png" alt="" data-size="line">

**###Notice**: remember to connect the nodes by clicking first on the upstream node and then the downstream node.

You can view how to add edges in the **video** below.

{% embed url="https://www.youtube.com/watch?t=204s&v=ub-fv-0u10A" %}
Guidance on how to add edges
{% endembed %}

The **reservoir system** should look like the **figure** below.

<figure><img src="../../.gitbook/assets/image (198).png" alt=""><figcaption><p>The example reservoir system</p></figcaption></figure>

### **2.4  Set up the time step and and time horizon**

<figure><img src="../../.gitbook/assets/image (214).png" alt=""><figcaption><p><strong>Set up the time step and and time horizon</strong></p></figcaption></figure>

### **2.5   Rename the nodes to names that make sense with their contexts**

* the **Catchment** node to '_Example catchment_',
* the **Reservoir** node to '_Example reservoir_'
* the **Output** node to '_Example outlet_'.
* the **Link** nodes to '_Release_' and the other one '_Spill_'.

The figure below shows where to click to rename the catchment node. The same process can be repeated for all the other nodes.

<figure><img src="../../.gitbook/assets/image (199).png" alt=""><figcaption><p>Rename the catchment node</p></figcaption></figure>

### **2.6   Inputing data into the Catchment node**

Please go to the following link to find the time series data for this step.

[https://docs.google.com/spreadsheets/d/1MR1Xxk77gFzcY3J3r6c6g38UB8pd1HMY/edit?usp=sharing\&ouid=103362449956532179397\&rtpof=true\&sd=true](https://docs.google.com/spreadsheets/d/1MR1Xxk77gFzcY3J3r6c6g38UB8pd1HMY/edit?usp=sharing\&ouid=103362449956532179397\&rtpof=true\&sd=true)

* Click on the **Catchment node** and follow the clicks (red arrows shown in the sequence of figures below.

<figure><img src="../../.gitbook/assets/image (200).png" alt=""><figcaption><p>Click on the catchment node and then the edit button for the Flow attribute.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (201).png" alt="" width="375"><figcaption><p>The type of parameter to be used for the flow parameter should be set to PYWR Dataframe which is a time-series.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (202).png" alt=""><figcaption><p>Click 'OK' to accept the parameter type change.</p></figcaption></figure>

* In the Excel link you will have a time series. Please copy the first (or only time series if there is only one). Make sure to copy the dates as well.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

* Paste the time series into cell **A1** in the **Dataframe** tab

<figure><img src="../../.gitbook/assets/image (204).png" alt=""><figcaption><p>Paste inflow data</p></figcaption></figure>

* You should have a time series as shown below. Click **Save**.

<figure><img src="../../.gitbook/assets/image (206).png" alt=""><figcaption><p>Save inflow data</p></figcaption></figure>

### **2.7   Inputing data into the Example reservoir node**

* Click on the **Example reservoir node**
* Set the **max\_volume** to 25 Mm3. This is the maximum capacity for the dam in this tutorial.
* Set the **initial\_volume** to 15 Mm3. This is the storage level that the simulation starts with on the first time step.
* Set the **allocation penalty** to -200. Often reservoirs have a negative allocation penalty. Allocation penalties are often used to balance reservoir or other water source use in multi-reservoir and multi-source systems.

The attributes on the reservoir should look like those below:

<figure><img src="../../.gitbook/assets/image (207).png" alt=""><figcaption><p>Reservoir data</p></figcaption></figure>

### **2.8  Inputting data on the the Spill and Release Link nodes.**

* On the **Spill link** node set the 'Allocation penalty' to 1000

<figure><img src="../../.gitbook/assets/image (208).png" alt="" width="291"><figcaption><p>Spill allocation penalty setting</p></figcaption></figure>

* The **Release link** node should not have any data input.

<figure><img src="../../.gitbook/assets/image (209).png" alt="" width="294"><figcaption><p>Release link setting</p></figcaption></figure>

### **2.9   Run the model**

<figure><img src="../../.gitbook/assets/image (210).png" alt="" width="375"><figcaption><p>Run the model</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (211).png" alt="" width="375"><figcaption><p>Run the model</p></figcaption></figure>

### **2.10   See the calculated results**

* View the '**simulated\_volume**' of the reservoir node to see the reservoir storage volume over time.

<figure><img src="../../.gitbook/assets/image (215).png" alt=""><figcaption><p>Get calculated results</p></figcaption></figure>

* Click on the 'Plot' view.

<figure><img src="../../.gitbook/assets/image (217).png" alt=""><figcaption><p>View the reservoir volume</p></figcaption></figure>

The reservoir is seen to fill and remain full for most of the time horizon. This is the case becaues there is no demand on the reservoir nor are there any evaporation losses defined.

**To see a video on how to run the model and view outputs click here.**
