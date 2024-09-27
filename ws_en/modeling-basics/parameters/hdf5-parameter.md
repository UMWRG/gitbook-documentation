# HDF5 Parameter

## General Description

This Parameter reads array data from a PyTables HDF database.

The parameter reads data using the PyTables array interface and therefore does not require loading the entire dataset in to memory. This is useful for large model runs. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.TablesArrayParameter.html#pywr.parameters.TablesArrayParameter)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="409">Description</th><th>Required</th></tr></thead><tbody><tr><td>h5file</td><td>The tables file handle or filename to attach the CArray objects to. If a filename is given the object will open and close the file handles</td><td>Yes</td></tr><tr><td>node</td><td>Name of the node in the tables database to read data from</td><td>Yes</td></tr><tr><td>where</td><td>Path to read the node from</td><td>Yes</td></tr><tr><td>scenario</td><td>Scenario to use as the second index in the array</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
