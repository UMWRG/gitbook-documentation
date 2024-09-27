# Delay Node

## General Description

The **delay node** is a node that delays flow for a given number of timesteps or days. This node will be used when the water propagation time cannot be ignored, compared to the selected time scale. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.nodes.DelayNode.html).



## Primary Attributes

<table><thead><tr><th width="180.33333333333331">Name</th><th width="316">Description</th><th>Required</th></tr></thead><tbody><tr><td>allocation penalty</td><td>The cost per unit flow via the node</td><td>Optional</td></tr><tr><td>timesteps</td><td>Number of timesteps to delay the flow</td><td>Optional</td></tr><tr><td>days</td><td>Number of days to delay the flow. Specifying a number of days (instead of a number of timesteps) is only valid if the number of days is exactly divisible by the model timestep delta</td><td>Optional</td></tr><tr><td>initial_flow</td><td>Flow provided by node for initial timesteps prior to any delayed flow being available. This is constant across all delayed timesteps and any model scenarios. Default is 0.0</td><td>Optional</td></tr></tbody></table>



## Examples

coming soon...
