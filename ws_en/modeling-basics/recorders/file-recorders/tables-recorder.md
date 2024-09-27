# Tables Recorder

## General Description

A recorder that saves to PyTables CArray

This Recorder creates a CArray for every node passed to the constructor. Each CArray stores the data for all scenarios on the specific node. This is useful for analysis of Node statistics across multiple scenarios. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.TablesRecorder.html)

## Attributes

<table><thead><tr><th width="175">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>The model to record nodes from</td><td>Optional</td></tr><tr><td>h5file</td><td>The tables file handle or filename to attach the CArray objects to. If a filename is given the object will open and close the file handles</td><td>Required</td></tr><tr><td>nodes</td><td>Nodes to save in the tables database. Can be an iterable of Node objects or node names. It can also be a iterable of tuples with a node specific where keyword as the first item and a Node object or name as the second item. If an iterable of tuples is provided then the node specific where keyword is used in preference to the where keyword (see below)</td><td>Required</td></tr><tr><td>parameters</td><td>Parameters to save. Similar to the nodes keyword, except refers to Parameter objects or names thereof</td><td>Required</td></tr><tr><td>where</td><td>Default path to create the CArrays inside the database</td><td>Required</td></tr><tr><td>time</td><td>Default full node path to save a time tables.Table. If None no table is created</td><td>Optional</td></tr><tr><td>scenarios</td><td>Default full node path to save a scenarios tables.Table. If None no table is created</td><td>Optional</td></tr><tr><td>routes_flows</td><td>Relative (to <em>where</em>) node path to save the routes flow CArray. If None (default) no array is created</td><td>Optional</td></tr><tr><td>routes</td><td>Full node path to save the routes tables.Table. If None not table is created</td><td>Optional</td></tr><tr><td>filter_kwds</td><td>Filter keywords to pass to tables.open_file when opening a file</td><td>Required</td></tr><tr><td>mode</td><td>Model argument to pass to tables.open_file. Defaults to ‘w’</td><td>Optional</td></tr><tr><td>metadata</td><td>Dict of user defined attributes to save on the root node (<em>root._v_attrs</em>)</td><td>Required</td></tr><tr><td>create_directories</td><td>If a file path is given and create_directories is True then attempt to make the intermediate directories. This uses os.makedirs() underneath</td><td>Optional</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
