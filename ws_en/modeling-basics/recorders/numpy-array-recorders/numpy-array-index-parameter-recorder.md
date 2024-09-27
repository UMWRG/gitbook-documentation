# Numpy Array Index Parameter Recorder

## General Description

Recorder for timeseries information from an _IndexParameter_.

This class stores the value from a specific _IndexParameter_ for each time-step of a simulation. The data is saved internally using a memory view. The data can be accessed through the _data_ attribute or _to\_dataframe()_ method. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.NumpyArrayIndexParameterRecorder.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.core.Model</td><td>Yes</td></tr><tr><td>param</td><td>Parameter instance to record</td><td>Yes</td></tr><tr><td>temporal_agg_func</td><td>Aggregation function used over time when computing a value per scenario. This can be used to return, for example, the median flow over a simulation. For aggregation over scenarios see the <em>agg_func</em> keyword argument</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```