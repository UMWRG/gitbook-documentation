# Aggregated Recorder

## General Description

This Recorder is used to aggregate across multiple other Recorder objects.

The class provides a method to produce a complex aggregated recorder by taking the results of other records. The _.values()_ method first collects unaggregated values from the provided recorders. These are then aggregated on a per scenario basis and returned by this classes _.values()_ method. This method allows _AggregatedRecorder_ to be used as a recorder for in other _AggregatedRecorder_ instances.

By default the same _agg\_func_ function is used for both steps, but an optional _recorder\_agg\_func_ can undertake a different aggregation across scenarios. For example summing recorders per scenario, and then taking a mean of the sum totals.[ ](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.NumpyArrayNodeCurtailmentRatioRecorder.html)[API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.AggregatedRecorder.html#pywr.recorders.AggregatedRecorder)

## Attributes

<table><thead><tr><th width="155">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.core.Model</td><td>Optional</td></tr><tr><td>recorders</td><td>The other <em>Recorder</em> instances to perform aggregation over</td><td>Optional</td></tr><tr><td>agg_func</td><td>Scenario aggregation function to use when <em>aggregated_value</em> is called (default=”mean”)</td><td>Optional</td></tr><tr><td>recorder_agg_func</td><td>Recorder aggregation function to use when <em>aggregated_value</em> is called (default=`agg_func`)</td><td>Optional</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
