# HDF5 Parameter

## General Description

This Parameter reads array data from a PyTables HDF database.

The parameter reads data using the PyTables array interface and therefore does not require loading the entire dataset in to memory. This is useful for large model runs. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.TablesArrayParameter.html#pywr.parameters.TablesArrayParameter)

By storing HDF5 files in the "fixed" format, users can achieve optimal data access speeds, making HDF5 an effective tool for Pywr-scenarios that use DataFrames as parameters, where fast data retrieval is crucial. HDF5 files are read as a dictionary, where each key represents a pandas DataFrame. For example, the structure of an inflows.h5 file might contain three keys, each representing a different river. Each key holds three time series that can be assigned to a Pywr scenario of size 3.

If using h5 file DataFrame for running pywr-scenarios, please refer to [pywr-scenarios section](https://app.gitbook.com/o/tUkZkKm5QY0V6IeofRg4/s/ODCd8VK2OOl9jOdp5KFf/\~/changes/223/modeling-basics/scenarios/pywr-scenarios) in order to activate this feature

**Note:** The size of pywr-scenarios must match the number of keys in the h5 file

## Attributes

<table><thead><tr><th width="158">Name</th><th width="409">Description</th><th>Required</th></tr></thead><tbody><tr><td>h5file</td><td>The tables file handle or filename to attach the CArray objects to. If a filename is given the object will open and close the file handles</td><td>Yes</td></tr><tr><td>node</td><td>Name of the node in the tables database to read data from</td><td>Yes</td></tr><tr><td>where</td><td>Path to read the node from</td><td>Yes</td></tr><tr><td>scenario</td><td>Scenario to use as the second index in the array</td><td>Yes</td></tr></tbody></table>

## Example

<figure><img src="../../.gitbook/assets/image (306).png" alt=""><figcaption><p>Structure inflows.h5</p></figcaption></figure>

```json
{
	"key": "Catchment River 1",
	"scenario": "Climate Change",
	"type": "DataFrameParameter",
	"url": "inflows.h5",
	"index_col": "timestep",
	"parse_dates": true
}

```
