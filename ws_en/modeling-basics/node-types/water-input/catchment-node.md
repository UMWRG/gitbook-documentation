# Catchment Node

## General Description

The **catchment node** is an another kind of input node with a fixed inflow. Catchment nodes are often used to represent river or other type of inflow into the system. Any flow defined on them has to flow into the system.&#x20;

Ofthen inflow time series (e.g. Pywr dataframes) are defined on the _flow_ attribute to represent catchment inflows however other parameters can also be used (e.g. constant, monthly profile etc...).

[API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.domains.river.Catchment.html).

## Primary Attributes

<table><thead><tr><th width="180.33333333333331">Name</th><th width="318">Description</th><th>Required</th></tr></thead><tbody><tr><td>flow</td><td>The amount of water supplied by the catchment node at each timestep</td><td>Required, defaults to 0 if not entered.</td></tr></tbody></table>



## Examples

coming soon...
