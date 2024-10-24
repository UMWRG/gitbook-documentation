# Pywr-Scenarios

Pywr Scenarios offer a more advanced and comprehensive approach to water management modeling, particularly when working with uncertainty and asessing various combinations of data and system behaviors and data inputs. Unlike WaterStrategy Scenarios, which focus on localized adjustments, Pywr Scenarios allow you to experiment with a wide range of possibilities by varying multiple inputs and combinations simultaneously.

In Pywr Scenarios:

* Users can define multiple scenarios, with each scenario containing multiple variations (or sizes).
* The system will simulate all combinations of these variations unless a specific combination is selected for simulation.

For example, if two Pywr Scenarios are defined, each with three variations (size = 3), the total number of simulations will be 9 (3 x 3). This approach enables users to explore a wide range of potential outcomes and interactions between different factors in the model.



## 1.  Activating Pywr Scenarios

In a Network, click on _View Network Data_ icon <img src="../../../.gitbook/assets/image (13).png" alt="" data-size="line">

This will open the right panel. In the section **Inputs**, type "_scenarios"_ and click on _Add an Input_ icon <img src="../../../.gitbook/assets/image (14).png" alt="" data-size="line">

<figure><img src="../../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

A window will be displayed, type "_scenarios"_, select the **scenarios** attribute and click **Save** as shown in the following image

<figure><img src="../../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

A new window will pop up, select **PYWR\_SCENARIOS** and click **Save**

<figure><img src="../../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>



## 2.  Creating pywr-scenarios

Once the scenario customization panel is open, you can define as many Pywr Scenarios as needed. To create a new Pywr Scenario, follow these steps:

Click <img src="../../../.gitbook/assets/image (19).png" alt="" data-size="line">



<figure><img src="../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

Edit the current default scenario by clicking on <img src="../../../.gitbook/assets/image (22).png" alt="" data-size="line">

Enter a **Name** for the Pywr-Scenario and specify the **Size** (number of variations).

The **Ensembles** attribute is optional and helps keep track of specific index scenarios within the Pywr Scenario

<figure><img src="../../../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

After creating the pywr-scenarios, the system will display the following information:

<figure><img src="../../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

Clicking on the **JSON** tab will display the automatic JSON version of the **Pywr-Scenario** definition

<figure><img src="../../../.gitbook/assets/image (25).png" alt="" width="409"><figcaption></figcaption></figure>

To load the data as h5 DataFrameParameter, please refer to [HDF5 Parameter section](../../parameters/hdf5-parameter.md) in order to access properly to the scenario data
