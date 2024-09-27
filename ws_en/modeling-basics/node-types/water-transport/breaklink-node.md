# BreakLink Node

## General Description

The **BreakLink node** can be used to reduce the number of routes in a model.&#x20;

For instance, in a model with form (3, 1, 3), i.e. 3 (A, B, C) inputs connected to 3 outputs (D, E, F) via a bottleneck (X), there are 3\*3 routes = 9 routes.

```
A -->\ /--> D
B --> X --> E
C -->/ \--> F
```

If X is a storage, there are only 6 routes: A->X\_o, B->X\_o, C->X\_o and X\_i->D\_o, X\_i->E\_o, X\_i->F\_o.

The BreakLink node is a compound node composed of a [Storage](../water-storage/storage-node.md) with zero volume and a [Link](link-node.md). It can be used in place of a normal Link, but with the benefit that it reduces the number of routes in the model (in the situation described above). The resulting LP is easier to solve. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.nodes.BreakLink.html#pywr.nodes.BreakLink).



## Primary Attributes

<table><thead><tr><th width="180.33333333333331">Name</th><th width="318">Description</th><th>Required</th></tr></thead><tbody><tr><td>allocation penalty</td><td>The cost per unit flow via the node</td><td>Optional</td></tr><tr><td>conversion_factor</td><td>The conversion between inflow and outflow for the node</td><td>Optional</td></tr><tr><td>max_flow</td><td>The maximum flow constraint on the node</td><td>Optional</td></tr><tr><td>min_flow</td><td>The minimum flow constraint on the node</td><td>Optional</td></tr><tr><td>prev_flow</td><td>Total flow via this node in the previous timestep</td><td>Optional</td></tr></tbody></table>



## Examples
