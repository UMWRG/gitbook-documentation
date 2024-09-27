# Index Parameter Recorder

## General Description

[API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.IndexParameterRecorder.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="487">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.core.Model</td><td>Yes</td></tr><tr><td>param</td><td>The parameter to record</td><td>Yes</td></tr><tr><td>agg_func</td><td>Scenario aggregation function to use when <em>aggregated_value</em> is called</td><td>Yes</td></tr><tr><td>name</td><td>Name of the recorder</td><td>Yes</td></tr><tr><td>comment</td><td>Comment or description of the recorder</td><td>Yes</td></tr><tr><td>ignore_nan</td><td>Flag to ignore NaN values when calling <em>aggregated_value</em></td><td>Yes</td></tr><tr><td>is_objective</td><td>Flag to denote the direction, if any, of optimisation undertaken with this recorder</td><td>Yes</td></tr><tr><td>epsilon</td><td>Epsilon distance used by some optimisation algorithms</td><td>Yes</td></tr><tr><td>constraint_lower_bounds, constraint_upper_bounds</td><td><p>The value(s) to use for lower and upper bound definitions. These values determine whether the recorder instance is marked as a constraint. Either bound can be <em>None</em> (the default) to disable the respective bound. If both bounds are <em>None</em> then the <em>is_constraint</em> property will return <em>False</em>. The lower bound must be strictly less than the upper bound. An equality constraint can be created by setting both bounds to the same value.</p><p>The constraint bounds are not used during model simulation. Instead they are intended for use by optimisation wrappers (or other external tools) to define constrained optimisation problems.</p></td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
