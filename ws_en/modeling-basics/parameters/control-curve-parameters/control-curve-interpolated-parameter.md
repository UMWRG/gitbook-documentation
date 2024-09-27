# Control Curve Interpolated Parameter

## General Description

A control curve Parameter that interpolates between three or more values.

Return values are linearly interpolated between control curves, with the first and last value being 100% and 0% respectively. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.control\_curves.ControlCurveInterpolatedParameter.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>storage_node</td><td>An optional <em>Storage</em> node that can be used to query the current percentage volume</td><td>Yes</td></tr><tr><td>control_curves</td><td>The Parameter objects to use as a control curve(s)</td><td>Yes</td></tr><tr><td>values</td><td>A list of values to return corresponding to the control curves. The length of the list should be 2 + len(control_curves)</td><td>Yes</td></tr><tr><td>parameters</td><td>If <em>values</em> is <em>None</em> then <em>parameters</em> can specify a <em>Parameter</em> object to use at each of the control curves. The number of parameters should be 2 + len(control_curves)</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
