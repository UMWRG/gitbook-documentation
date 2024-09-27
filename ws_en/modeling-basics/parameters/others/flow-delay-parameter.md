# Flow Delay Parameter

## General Description

Parameter that returns the delayed flow for a node after a given number of timesteps or days. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.FlowDelayParameter.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.model.Model</td><td>Yes</td></tr><tr><td>node</td><td>The node to delay for</td><td>Yes</td></tr><tr><td>timesteps</td><td>Number of timesteps to delay the flow</td><td>Yes</td></tr><tr><td>days</td><td>Number of days to delay the flow. Specifying a number of days (instead of a number of timesteps) is only valid if the number of days is exactly divisible by the model timestep length</td><td>Yes</td></tr><tr><td>initial_flow</td><td>Flow value to return for initial model timesteps prior to any delayed flow being available. This value is constant across all delayed timesteps and any model scenarios. Default is 0.0</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
