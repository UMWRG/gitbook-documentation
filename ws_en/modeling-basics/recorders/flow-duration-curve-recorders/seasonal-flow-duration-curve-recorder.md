# Seasonal Flow Duration Curve Recorder

## General Description

This recorder calculates a flow duration curve for each scenario for a given season specified in months. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.SeasonalFlowDurationCurveRecorder.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.core.Model</td><td>Yes</td></tr><tr><td>node</td><td>The node to record</td><td>Yes</td></tr><tr><td>percentiles</td><td>The percentiles to use in the calculation of the flow duration curve. Values must be in the range 0-100</td><td>Yes</td></tr><tr><td>agg_func</td><td>Function used for aggregating the FDC deviations across percentiles. Numpy style functions that support an axis argument are supported</td><td>Yes</td></tr><tr><td>fdc_agg_func</td><td>Optional different function for aggregating across scenarios</td><td>Yes</td></tr><tr><td>months</td><td>The numeric values of the months the flow duration curve should be calculated for</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
