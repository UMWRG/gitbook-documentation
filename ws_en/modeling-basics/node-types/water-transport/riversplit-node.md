# RiverSplit Node

## General Description

The **RiverSplit node** is a split in the river network. It is intended for a simple case of where fixed ratio of flow is required to be distributed to multiple downstream routes. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.domains.river.RiverSplit.html).

## Primary Attributes

<table><thead><tr><th width="180.33333333333331">Name</th><th width="355">Description</th><th>Required</th></tr></thead><tbody><tr><td>factors</td><td>The factors to force on the additional splits. Number of extra_slot is assumed to be one less than the length of factors (as per <em>pywr.nodes.MultiSplitLink</em> documentation).</td><td>Optional</td></tr><tr><td>slot_names</td><td>The identifiers to refer to the slots when connect from this Node. Length must be one more than the number of extra slots required.</td><td>Optional</td></tr></tbody></table>



## Examples

coming soon...
