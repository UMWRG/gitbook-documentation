# PiecewiseLink Node

## General Description

The **PiecewiseLink node** is an extension of Node that represents a non-linear [Link](link-node.md) with a piece wise cost function. This object is intended to model situations where there is a benefit of supplying certain flow rates but beyond a fixed limit there is a change in (or zero) cost. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.nodes.PiecewiseLink.html).

This Node is implemented using a compound node structure like so:

```
        | Separate Domain         |
Output -> Sublink 0 -> Sub Output -> Input
       -> Sublink 1 ---^
       ...             |
       -> Sublink n ---|
```

This means routes do not directly traverse this node due to the separate domain in the middle. Instead several new routes are made for each of the sublinks and connections to the Output/Input node. The reason for this breaking of the route is to avoid an geometric increase in the number of routes when multiple PiecewiseLinks are present in the same route.

## Primary Attributes

<table><thead><tr><th width="180.33333333333331">Name</th><th width="318">Description</th><th>Required</th></tr></thead><tbody><tr><td>allocation penalty</td><td>The cost per unit flow via the node</td><td>Optional</td></tr><tr><td>max_flow</td><td>The maximum flow constraint on the node</td><td>Optional</td></tr><tr><td>min_flow</td><td>The minimum flow constraint on the node</td><td>Optional</td></tr></tbody></table>



## Examples

coming soon...
