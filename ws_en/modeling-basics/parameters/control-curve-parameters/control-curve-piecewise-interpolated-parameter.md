# Control Curve Piecewise Interpolated Parameter

## General Description

A control curve Parameter that interpolates between two or more pairs of values.

Return values are linearly interpolated between a pair of values depending on the current storage. The first pair is used between maximum and the first control curve, the next pair between the first control curve and second control curve, and so on until the last pair is used between the last control curve and the minimum value. The first value in each pair is the value at the upper position, and the second the value at the lower position. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.control\_curves.ControlCurvePiecewiseInterpolatedParameter.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>storage_node</td><td>The storage node to compare the control curve(s) to</td><td>Yes</td></tr><tr><td>control_curves</td><td>A list of parameters representing the control curve(s). These are often MonthlyProfileParameters or DailyProfileParameters, but may be any Parameter that returns values between 0.0 and 1.0. If floats are passed they are converted to <em>ConstantParameter</em></td><td>Yes</td></tr><tr><td>values</td><td>A list of value pairs to interpolate between. The length of the list should be 1 + len(control_curves)</td><td>Yes</td></tr><tr><td>minimum</td><td>The storage considered the bottom of the lower curve, 0-1 (default=0)</td><td>Yes</td></tr><tr><td>maximum</td><td>The storage considered the top of the upper curve, 0-1 (default=1)</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
