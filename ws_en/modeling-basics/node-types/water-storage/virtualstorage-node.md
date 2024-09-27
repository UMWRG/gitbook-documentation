# VirtualStorage Node

## General Description

The **VirtualStorage node** is a virtual storage unit. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.nodes.VirtualStorage.html).

Notes:

TODO: The cost property is not currently respected. See issue #242.

## Primary Attributes

<table><thead><tr><th width="180.33333333333331">Name</th><th width="318">Description</th><th>Required</th></tr></thead><tbody><tr><td>allocation penalty</td><td>The cost per unit flow via the node</td><td>Optional</td></tr><tr><td>nodes</td><td>List of inflow/outflow nodes that affect the storage volume</td><td>Required</td></tr><tr><td>min_volume</td><td>The minimum volume the storage is allowed to reach</td><td>Optional</td></tr><tr><td>max_volume</td><td>The maximum volume of the storage</td><td>Required,  defaults to 0 if not entered</td></tr><tr><td>initial_volume</td><td>The initial storage volume</td><td>One is required</td></tr><tr><td>factors</td><td>List of factors to multiply node flow by. Positive factors remove water from the storage, negative factors remove it.</td><td>Optional</td></tr></tbody></table>



## Examples

coming soon...
