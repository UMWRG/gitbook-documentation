---
description: An overview of Pywr recorders supported by WaterStrategy
---

# Recorders

This page describes the process of creating a new Recorder in WaterStrategy and a selection of the most commonly used Pywrrecorder types, and most commonly used attributes.  The full list of built-in recorders and their exhaustive list of attributes are [here](https://pywr.github.io/pywr-docs/master/api/pywr.recorders.html).

## 1. Creating a Recorder in WaterStrategy

In a Network page, click the 'Recorders' Tab:

<figure><img src="../../.gitbook/assets/image (47).png" alt=""><figcaption><p>CLick the 'Recorders' Tab</p></figcaption></figure>

Next to the 'Recorders-Type Categories' Text, click the '+' button and select 'PYWR\_RECORDER':\


<figure><img src="../../.gitbook/assets/Screenshot 2024-07-09 091615.png" alt=""><figcaption></figcaption></figure>

Enter the name of your recorder. This can be anything you like, <mark style="color:red;">**but must be unique within the network**</mark>**.**

<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

Populate the recorder in the JSON editor:

<figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

## 2. Recorder editors in WaterStrategy

Currently, there are two different ways to input a Recorder in WaterStrategy. ....

## 3. NumpyArrayNodeRecorder

Recorder for timeseries information from a Node.  [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.NumpyArrayNodeRecorder.html#pywr.recorders.NumpyArrayNodeRecorder)

This class stores flow from a specific node for each time-step of a simulation. The results of a recorder are output on the Network Attributes panel, and will be named 'simulated\_\<recordername>'

### 3.1. Attributes

<table><thead><tr><th width="196">Name</th><th width="243">Description</th><th>Required</th><th>Default value</th></tr></thead><tbody><tr><td>type</td><td>numpyarraynoderecorder</td><td>Yes</td><td>None</td></tr><tr><td>node</td><td>Name of the node to record</td><td>Yes</td><td>None</td></tr><tr><td>temporal_agg_func</td><td></td><td>Optional</td><td>mean</td></tr><tr><td>agg_func</td><td></td><td>Optional</td><td>mean</td></tr></tbody></table>

### 3.2. Example

```json
{
	"type": "NumpyArrayNodeRecorder",
	"node": "Reservoir 1",
	"temporal_agg_func": "mean",
	"agg_func": "mean"
}
```
