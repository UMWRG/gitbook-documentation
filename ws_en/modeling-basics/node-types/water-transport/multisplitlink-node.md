# MultiSplitLink Node

## General Description

The **MultiSplitLink node** is an extension of [PiecewiseLink](https://app.gitbook.com/o/tUkZkKm5QY0V6IeofRg4/s/ODCd8VK2OOl9jOdp5KFf/\~/changes/91/modelling-fundamentals/node-types/water-transport/piecewiselink-node) that includes additional slots to connect from.

Conceptually this node looks like the following internally,

```
         / -->-- X0 -->-- \
A -->-- Xo -->-- X1 -->-- Xi -->-- C
         \ -->-- X2 -->-- /
                 |
                 Bo -->-- Bi --> D
```

An additional sublink in the PiecewiseLink (i.e. X2 above) and nodes (i.e. Bo and Bi) in this class are added for each extra slot.

Finally a mechanism is provided to (optionally) fix the ratio between the last non-split sublink (i.e. X1) and each of the extra sublinks (i.e. X2). This mechanism uses _AggregatedNode_ internally. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.nodes.MultiSplitLink.html).

Notes: Users must be careful when using the factor mechanism. Factors use the last non-split sublink (i.e. X1 but not X0). If this link is constrained with a maximum or minimum flow, or if it there is another unconstrained link (i.e. if X0 is unconstrained) then ratios across this whole node may not be enforced as expected.

## Primary Attributes

<table><thead><tr><th width="180.33333333333331">Name</th><th width="318">Description</th><th>Required</th></tr></thead><tbody><tr><td>allocation penalty</td><td>The cost per unit flow via the node</td><td>Optional</td></tr><tr><td>max_flow</td><td>The maximum flow constraint on the node</td><td>Optional</td></tr><tr><td>extra_slots</td><td>Number of additional slots (and sublinks) to provide. Must be greater than zero.</td><td>Optional</td></tr><tr><td>slot_names</td><td>The names by which to refer to the slots during connection to other nodes. Length must be one more than the number of extra_slots. The first item refers to the PiecewiseLink connection with the following items for each extra slot.</td><td>Optional</td></tr><tr><td>factors</td><td>If given, the length must be equal to one more than the number of extra_slots. Each item is the proportion of total flow to pass through the additional sublinks. If no factor is required for a particular sublink then use <em>None</em> for its items. Factors are normalised prior to use in the solver.</td><td>Optional</td></tr></tbody></table>



## Examples

coming soon...
