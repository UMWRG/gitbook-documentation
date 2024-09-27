# Input Node

## General Description

Input nodes represent water inputs into the system.&#x20;

At each time step an input node can provide as much water as set by the **Max Flow** attribute. However, unlike [Catchment nodes](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/node-types/catchment-node) which are required to release the volume of water that is defined in their Flow attribute,  input nodes are not required to release any water unless they have a non-zero **Min Flow**.

Input nodes are often used to represent sources that are defined by yields. They are often used to represent groundwater yields.

[API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.nodes.Input.html).

## Primary Attributes

<table><thead><tr><th width="181.33333333333331">Name</th><th width="342">Description</th><th>Required</th></tr></thead><tbody><tr><td>Allocation Penalty</td><td>The alllocation cost per unit flow via the node</td><td>Optional</td></tr><tr><td>Max Flow</td><td>The maximum flow constraint on the node</td><td>Optional</td></tr><tr><td>Min Flow</td><td>The minimum flow constraint on the node</td><td>Optional</td></tr></tbody></table>

## Examples

coming soon...
