# Adding monthly evaporation and rainfall

In this step, we will add the the Evaporation and Precipitation rates (mm/day). Internally the reservoir multiplies the real-time Reservoir area by the Evaportion.

The Evaporation can be defined by a parameter or a scalar. For example, a time series can be used that is correlated to the flow scenario time series. However in this case, we will use a [Monthly profile parameter](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/monthly-profile) which assigns a different value to each month in the year.

1. Select the reservoir and edit the Evaporation attribute.

<figure><img src="../../../.gitbook/assets/image (101).png" alt=""><figcaption><p>Edit the Evaporation attribute</p></figcaption></figure>

2. WaterStrategy has a Json editor for a Monthly profile parameter. To use it, In the options tab select **PYWR\_MONTHLY\_PROFILE**.

<figure><img src="../../../.gitbook/assets/image (103).png" alt="" width="375"><figcaption><p>Select PYWR_MONTHLY_PROFILE</p></figcaption></figure>

3. In the **Monthly Profile tab**, enter the evaporation rates in the table below:

<table><thead><tr><th width="146"></th><th width="67">Jan</th><th width="68">Feb</th><th width="65">Mar</th><th width="63">Apr</th><th width="67">May</th><th width="64">Jun</th><th width="68">Jul</th><th width="69">Aug</th><th width="67">Sep</th><th width="66">Oct</th><th width="63">Nov</th><th width="100">Dec</th></tr></thead><tbody><tr><td>Evaporation (mm/day)</td><td>2.70</td><td>4.02</td><td>1.45</td><td>1.98</td><td>0.98</td><td>0.10</td><td>0.04</td><td>0.03</td><td>0.04</td><td>0.48</td><td>1.14</td><td>2.45</td></tr></tbody></table>

<figure><img src="../../../.gitbook/assets/image (105).png" alt=""><figcaption><p>Enter the evaporation</p></figcaption></figure>

Then, save it.

4. Follow the same steps for the Rainfall attribute using the table below the figure.

<figure><img src="../../../.gitbook/assets/image (106).png" alt=""><figcaption><p>Edit the Rainfall</p></figcaption></figure>

<table><thead><tr><th width="142"></th><th width="66">Jan</th><th width="68">Feb</th><th width="64">Mar</th><th width="67">Apr</th><th width="67">May</th><th width="64">Jun</th><th width="64">Jul</th><th width="73">Aug</th><th width="67">Sep</th><th width="68">Oct</th><th width="64">Nov</th><th>Dec</th></tr></thead><tbody><tr><td>Precipitation (mm/day)</td><td>4.91</td><td>2.33</td><td>1.24</td><td>2.30</td><td>0.39</td><td>0.01</td><td>0.01</td><td>0.00</td><td>0.01</td><td>0.48</td><td>1.76</td><td>2.23</td></tr></tbody></table>

5. Finally set the **Evaporation Penalty** to -2000 and the **Evaporation Unit Conversion** on the reservoir node to 0.001.

<figure><img src="../../../.gitbook/assets/image (107).png" alt=""><figcaption><p>Set the  Evaporation Penalty and Evaporation Unit Conversion</p></figcaption></figure>

The highly negative Evaporation Penalty of -2000 is higher priority than either the reservoir and any other nodes in the system. This ensures that **evaporation outflow** is met first **before** any management rules are implemented.

The **Unit Conversion** allows the model to correctly convert the evaporation in mm/day and reservoir area in Km2 to the correct flow units in the template which are Mm3/day

6. Run this scenario and compare the simulated volume against the **'Demand with GW'** scenario.

Evaporation is shown to result in a decrease in reservoir levels during droughts. Precipitation additions do not compensate for the losses.

<figure><img src="../../../.gitbook/assets/image (119).png" alt=""><figcaption><p>Reservoir volume compare</p></figcaption></figure>
