# RiverSplitWithGauge Node

## General Description

The **RiverSplitWithGauge node** is a split in the river network with a minimum residual flow (MRF). As per _RiverSplit_ but by default creates another route in the underlying object to model a MRF. This route is such that the MRF is not part of forced ratios. The intent of this object is to model the case where a proportion of flow can be abstracted above the MRF (e.g. 90% of flow above MRF). [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.domains.river.RiverSplitWithGauge.html).

## Primary Attributes

<table><thead><tr><th width="152.33333333333331">Name</th><th width="397">Description</th><th>Required</th></tr></thead><tbody><tr><td>mrf</td><td>The minimum residual flow (MRF) at the gauge</td><td>Required</td></tr><tr><td>mrf_cost</td><td>The cost of the route via the MRF</td><td>Required</td></tr><tr><td>cost</td><td>The cost of the other (unconstrained) route</td><td>Required</td></tr><tr><td>factors</td><td>The factors to force on the additional splits. Number of extra_slot is assumed to be one less than the length of factors (as per <em>MultiSplitLink</em> documentation)</td><td>Required</td></tr><tr><td>slot_names</td><td>The identifiers to refer to the slots when connect from this Node. Length must be one more than the number of extra slots required</td><td>Required</td></tr></tbody></table>



## Examples

coming soon...
