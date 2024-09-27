# Numpy Array Node Supplied Ratio Recorder

## General Description

Recorder for timeseries of ratio of supplied flow from a _Node._ This class stores supply ratio from a specific node for each time-step of a simulation. The data is saved internally using a memory view. The data can be accessed through the _data_ attribute or _to\_dataframe()_ method.[ API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.NumpyArrayNodeSuppliedRatioRecorder.html)

```
supply_ratio = actual_flow / max_flow
```

## Attributes

<table><thead><tr><th width="155">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td></td><td></td></tr><tr><td>node</td><td>Node instance to record</td><td>Optional</td></tr><tr><td>temporal_agg_func</td><td>Aggregation function used over time when computing a value per scenario. This can be used to return, for example, the median flow over a simulation. For aggregation over scenarios see the <em>agg_func</em> keyword argument</td><td>Optional</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
