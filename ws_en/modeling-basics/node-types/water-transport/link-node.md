# Link Node

## General Description

The **link node** represents a link in the water system or other point of interest where a maximum or minimum flow constraint or an allocation priority are assigned. Please note in Pywr, Edges (Links) cannot be assigned flow constraintes and therefore link nodes are often used for this purpose.  [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.nodes.Link.html).



## Primary Attributes

<table><thead><tr><th width="181.33333333333331">Name</th><th width="342">Description</th><th>Required</th></tr></thead><tbody><tr><td>allocation penalty</td><td>The cost per unit flow via the node</td><td>Optional</td></tr><tr><td>max_flow</td><td>The maximum flow constraint on the node</td><td>Optional</td></tr><tr><td>min_flow</td><td>The minimum flow constraint on the node</td><td>Optional</td></tr></tbody></table>



## Examples

coming soon...
