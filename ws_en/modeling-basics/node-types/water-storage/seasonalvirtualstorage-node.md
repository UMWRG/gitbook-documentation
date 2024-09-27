# SeasonalVirtualStorage Node

## General Description

The **SeasonalVirtualStorage node** is a virtual storage node that operates only for a specified period within a year.

This node is most useful for representing licences that are only enforced during specified periods. The _reset\_day_ and _reset\_month_ parameters indicate when the node starts operating and the _end\_day_ and _end\_month_ when it stops operating. For the period when the node is not operating, the volume of the node remains unchanged and the node does not apply any constraints to the model.

The end\_day and end\_month can represent a date earlier in the year that the reset\_day and and reset\_month. This situation represents a licence that operates across a year boundary. For example, one that is active between October and March and not active between April and September.[API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.nodes.SeasonalVirtualStorage.html).

## Primary Attributes

<table><thead><tr><th width="167.33333333333331">Name</th><th width="384">Description</th><th>Required</th></tr></thead><tbody><tr><td>reset_day</td><td>The day of the month (0-31) when the node starts operating and its volume is reset to the initial value or maximum volume.</td><td>Required</td></tr><tr><td>reset_month</td><td>The month of the year (0-12) when the node starts operating and its volume is reset to the initial value or maximum volume.</td><td>Required</td></tr><tr><td>reset_to_initial_volume</td><td>Reset the volume to the initial volume instead of maximum volume each year (default is False)</td><td>Required</td></tr><tr><td>end_day</td><td>The day of the month (0-31) when the node stops operating</td><td>Required</td></tr><tr><td>end_month</td><td>The month of the year (0-12) when the node stops operating</td><td>Required</td></tr></tbody></table>

## Examples

coming soon...
