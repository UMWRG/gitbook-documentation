# AggregatedNode

## General Description

The **AggregatedNode node** is an aggregated sum of other _Node_ nodes.

This object should behave like _Node_ by returning current _flow_. However this object can not be connected to others within the network. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.nodes.AggregatedNode.html).

Notes: This node can not be connected to other nodes in the network.

## Primary Attributes

<table><thead><tr><th width="180.33333333333331">Name</th><th width="318">Description</th><th>Required</th></tr></thead><tbody><tr><td>model </td><td>`Model` instance</td><td>Required</td></tr><tr><td>name</td><td>str</td><td>Required</td></tr><tr><td>storage_nodes</td><td>The <em>Node</em> objects which to return the sum total of</td><td>Required</td></tr></tbody></table>

## Examples

coming soon...
