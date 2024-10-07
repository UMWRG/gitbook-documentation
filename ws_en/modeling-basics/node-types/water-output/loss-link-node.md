# Loss Link Node

## General description

A **loss link** allows for the definition of a fixed proportional loss of flow that goes through this node.  Loss links are often used to represent **potable water treatment works** which incur some process losses.

The Max and Min flow attributes that are defined are applied to the net output after losses.&#x20;

The node itself records the net output in its flow attribute (which would be used by any attached recorders).

## Primary Attributes

<table><thead><tr><th width="181.33333333333331">Name</th><th width="342">Description</th><th>Required</th></tr></thead><tbody><tr><td>Allocation Penalty</td><td>The cost per unit flow via the node</td><td>Optional</td></tr><tr><td>Loss factor</td><td>loss_factor : float or Parameter. The proportion of flow that is lost through this node. Must be greater than or equal to zero. This value is either a proportion of gross or net flow depending on the value of <code>loss_factor_type</code>.</td><td>Optional, defaults to 0</td></tr><tr><td>Loss Factor Type</td><td>Either "gross" or "net" (default) to specify whether the loss factor is applied as a proportion of gross or net flow respectively.</td><td>Optional, defaults to "net" </td></tr><tr><td>Max Flow</td><td>The maximum flow constraint on the node</td><td>Optional</td></tr><tr><td>Min Flow</td><td>The minimum flow constraint on the node</td><td>Optional</td></tr></tbody></table>



## Example

<figure><img src="../../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

In this example 10% of the gross amount of water flowing into the node is lost.
