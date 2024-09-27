# Flow Duration Curve Deviation Recorder

## General Description

This recorder calculates a Flow Duration Curve (FDC) for each scenario and then calculates their deviation from upper and lower target FDCs. The 2nd dimension of the target duration curves and percentiles list must be of the same length and have the same order (high to low values or low to high values).

Deviation is calculated as positive if actual FDC is above the upper target or below the lower target. If actual FDC falls between the upper and lower targets zero deviation is returned. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.FlowDurationCurveDeviationRecorder.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.core.Model</td><td>Yes</td></tr><tr><td>node</td><td>The node to record</td><td>Yes</td></tr><tr><td>percentiles</td><td>The percentiles to use in the calculation of the flow duration curve. Values must be in the range 0-100</td><td>Yes</td></tr><tr><td>lower_target_fdc</td><td>The lower FDC against which the scenario FDCs are compared</td><td>Yes</td></tr><tr><td>upper_target_fdc</td><td>The upper FDC against which the scenario FDCs are compared</td><td>Yes</td></tr><tr><td>agg_func</td><td>Function used for aggregating the FDC deviations across percentiles. Numpy style functions that support an axis argument are supported</td><td>Yes</td></tr><tr><td>fdc_agg_func</td><td>Optional different function for aggregating across scenarios</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
