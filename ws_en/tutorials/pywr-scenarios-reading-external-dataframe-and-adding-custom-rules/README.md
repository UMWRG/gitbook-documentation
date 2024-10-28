# Pywr-scenarios reading external DataFrame and adding Custom Rules

In this tutorial, we will be working with the **Thames Network**, which is automatically generated when creating a WaterStrategy account.

The steps covered include:

1. **Updating Lee Valley Demand**: We will read and update the Lee Valley Demand data from an external CSV file containing a time series.
2. **Applying Climate Change Uncertainty**: Climate change uncertainties will be introduced by activating **pywr-scenarios**. These uncertainties will be applied to two catchment nodes (inflows), adjusting the inflow conditions based on specified scenarios.
3. **Adding a Custom Rule**: You will learn how to create a Custom Rule, a powerful tool that allows for the expansion and integration of WaterStrategy functionality. In this example, a new parameter will be created to dynamically increase the maximum volume of a reservoir on a specific date, as defined by the user.

By the end of this tutorial, you will be equipped to manage and customize various aspects of the Thames network within WaterStrategy, utilizing time series data, uncertainty scenarios, and custom rules.

You will manually upload the required files, so make sure to save them on your computer for easy access during the tutorial

* [Thames\_Lee\_Valley\_demand](https://nexsysanalytics-my.sharepoint.com/:x:/g/personal/jgonzalez\_nexsys-analytics\_com/ERY5QXJtGQtFpo7PKUUykJEBI9g6adLvCwxG90xhZqgySQ?e=b4brjW)
* [Thames\_inflows\_pywrScenarios.h5](https://nexsysanalytics-my.sharepoint.com/:u:/g/personal/jgonzalez\_nexsys-analytics\_com/EV7TBf9J\_WZDpF3Oy6HyNmoBj3F4Ew216OE9ltOCC1P8pw?e=YV1A3q)



To get started, in **Project Training Material**, open **Thames** network

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

Clone **Scenario 1**

<figure><img src="../../.gitbook/assets/image (27).png" alt="" width="375"><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (28).png" alt="" width="563"><figcaption></figcaption></figure>



