# Numpy Array Storage Recorder

## General Description

Recorder for timeseries information from a _Storage_ node.

This class stores volume from a specific node for each time-step of a simulation. The data is saved internally using a memory view. The data can be accessed through the _data_ attribute or _to\_dataframe()_ method. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.NumpyArrayStorageRecorder.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.core.Model</td><td>Yes</td></tr><tr><td>node</td><td>Node instance to record</td><td>Yes</td></tr><tr><td>proportional</td><td>Whether to record proportional [0, 1.0] or absolute storage volumes (default=False)</td><td>Yes</td></tr><tr><td>temporal_agg_func</td><td>Aggregation function used over time when computing a value per scenario. This can be used to return, for example, the median flow over a simulation. For aggregation over scenarios see the <em>agg_func</em> keyword argument</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
