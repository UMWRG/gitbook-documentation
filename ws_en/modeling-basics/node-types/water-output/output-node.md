# Output Node

## General Description

The **output node** ([API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.nodes.Output.html)) is a general output at any point from the network. Output nodes remove water from the system.&#x20;

Output nodes are required at the end of a river and in this use case generally do not have an allocation penalty or max\_flow assigned. &#x20;

Output nodes are also used to represent consumptive water demands. In this use case, they tend to have negative allocation penalties assigned so that the linear program allocates water to them as well as a max\_flow which can be either a constant or a parameter representing the water demand.



## Primary Attributes

<table><thead><tr><th width="181.33333333333331">Name</th><th width="342">Description</th><th>Required</th></tr></thead><tbody><tr><td>allocation penalty</td><td>The cost per unit flow via the node</td><td>Optional</td></tr><tr><td>max_flow</td><td>The maximum flow constraint on the node</td><td>Optional</td></tr><tr><td>min_flow</td><td>The minimum flow constraint on the node</td><td>Optional</td></tr></tbody></table>



## Examples

coming soon...
