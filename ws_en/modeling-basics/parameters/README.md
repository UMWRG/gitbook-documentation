---
description: An overview of Pywr parmeters supported by WaterStrategy
---

# Parameters

Paramters are functions that return a value in the model at each time-step. These values can be a constant, based on time (e.g., on the day or month), a calculation based on the time step's reservoir storage and many other calculations. Custom parameter can also be written in Python.

This page describes (most of) the parameter types supported by Pywr. An overview of parameters in Pywr can be found [here](https://pywr.github.io/pywr-docs/master/json.html#parameters).  The full list of built-in Pywr parameters are found [here](https://pywr.github.io/pywr-docs/master/api/pywr.parameters.html).

## 1. Creating a Parameter

In a Network, click the 'Parameters' Tab:

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption><p>CLick the 'parameters' tab</p></figcaption></figure>

Next to the 'Parameters-Type Categories' section, click the '+' button and select 'PYWR\_PARAMETER'.

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption><p>Click on pywr_parameter</p></figcaption></figure>

A text-input will appear. Enter the name of your parameter:\


<figure><img src="../../.gitbook/assets/image (54).png" alt=""><figcaption><p>Enter the parameter name</p></figcaption></figure>

Modify the parameter as required in the JSON editor provided:

<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

## 2. Parameter editors in WaterStrategy

To make parameter modifications simpler, WaterStrategy offers editors for commonly used Parameters, such as Monthly Profile parameters, with pre-populated default values, and graphical editors to make entering of data simpler.&#x20;

#### Example parameter editor

In the Parameters Tab, when adding a new Parameter, select 'PYWR\_PARAMETER\_MONTHLY\_PROFILE' as shown:\


<figure><img src="../../.gitbook/assets/image (56).png" alt=""><figcaption><p>Select PYWR_PARAMETER_MONTHLY_PROFILE</p></figcaption></figure>

Note that the edior which appears will show a JSON tab, but also a Plot and Table tab. Modifying the data in the table will automaticall update the data in the JSON as shown:\


<figure><img src="../../.gitbook/assets/image (57).png" alt=""><figcaption><p>Note the values have been edited in a spreadsheet editor</p></figcaption></figure>

These changes automatically update the JSON:

<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption><p>Data is automatically updated in the JSON section</p></figcaption></figure>

##
