# Numpy Array Daily Profile Parameter Recorder

## General Description

Recorder for an annual profile from a _Parameter_.

This recorder stores a daily profile returned by a specific parameter. For each day of the year it stores the value encountered for that day during a simulation. This results in the final profile being the last value encountered on each day of the year during a simulation. This recorder is useful for returning the daily profile that may result from the combination of one or more parameters. For example, during optimisation of new profiles non-daily parameters (e.g. _RbfProfileParameter_) and/or aggregations of several parameters might be used. With this recorder the daily profile used in the simulation can be easily saved.

The data is saved internally using a memory view. The data can be accessed through the _data_ attribute or _to\_dataframe()_ method. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.NumpyArrayDailyProfileParameterRecorder.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.core.Model</td><td>Yes</td></tr><tr><td>param</td><td>Parameter instance to record</td><td>Yes</td></tr><tr><td>temporal_agg_func</td><td>Aggregation function used over time when computing a value per scenario. For aggregation over scenarios see the <em>agg_func</em> keyword argument</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
