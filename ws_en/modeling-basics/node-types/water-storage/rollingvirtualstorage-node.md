# RollingVirtualStorage  Node

## General Description

The **RollingVirtualStorage node** is a rolling virtual storage node useful for implementing rolling licences. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.nodes.RollingVirtualStorage.html).

Notes:

TODO: The cost property is not currently respected. See issue #242.

## Primary Attributes

<table><thead><tr><th width="180.33333333333331">Name</th><th width="318">Description</th><th>Required</th></tr></thead><tbody><tr><td>allocation penalty</td><td>The cost per unit flow via the node</td><td>Optional</td></tr><tr><td>nodes</td><td>List of inflow/outflow nodes that affect the storage volume</td><td>Required</td></tr><tr><td>min_volume</td><td>The minimum volume the storage is allowed to reach</td><td>Optional</td></tr><tr><td>max_volume</td><td>The maximum volume of the storage</td><td>Required,  defaults to 0 if not entered</td></tr><tr><td>initial_volume</td><td>The initial storage volume</td><td>One is required</td></tr><tr><td>factors</td><td>List of factors to multiply node flow by. Positive factors remove water from the storage, negative factors remove it.</td><td>Optional</td></tr><tr><td>timesteps</td><td>The number of timesteps to apply to the rolling storage over</td><td>Required</td></tr><tr><td>days</td><td>The number of days to apply the rolling storage over. Specifying a number of days (instead of a number of timesteps) is only valid with models running a timestep of daily frequency</td><td>Required</td></tr></tbody></table>



## Examples

coming soon...
