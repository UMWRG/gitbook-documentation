---
description: Key terms used in Pywr.
---

# Pywr Concepts

Pywr, a Python library used by WaterStrategy, enables simulating resource allocation by representing a resource system as a network using "Nodes" and "Links". Resource allocation is driven by operating rules using "Allocation Penalties," "Constraints," and "Parameters," and model outputs are captured and saved using "Recorders." Variations of model inputs can be specified and run in parallel using "Scenarios."

While the general concepts used to create a resource allocation simulation model in Pywr are similar to those of other tools, the use of terms can differ. In this section, we define key Pywr terms and their roles in simulation models.

## Node

Nodes represent locations of interest in the simulated system where water is added, stored, used, or transmitted. There are many different node types in Pywr to help you quickly build your water system model. It includes water input, water output, water transport, water storage, and so on. You can learn more about them in the [Node types](https://water-strategy.gitbook.io/water-strategy/modeling-basics/node-types) section. Some of the data that define the physical characteristics and behavior of a node can be added directly to the node or indirectly by referring to a parameter (described below).

## Edge

To form a network, nodes are connected using links that Pywr calls 'Edges'. An edge must have starting and ending nodes. Water flows from the starting node to the ending node. In contrast to other modelling tools, Pywr does not assign information to connections (i.e., Edges) except the source and destination nodes. All of the data required to perform the allocation procedure is stored on the nodes, and the structure of the Edges determines the direction of water flow.

## Constraint

Constraints can be set on various node types to help represent system behavior. For instance, a river node can have maximum and/or minimum flow values to represent the conveyance capacity. In Pywr, many nodes have the 'max\_flow' and 'min\_flow' attributes to set the upper and lower limits of the flow through the node if needed. The 'max\_flow' attribute doesn't require that the flow through this node reach this value, but if the water volume and priority are sufficient, the model will try to meet the 'Max Flow.' Minimum flow constraints should be used carefully as they can result in model infeasibility if the minimum cannot be met.

## Allocation Penalty or 'Cost'

Allocation penalties are node attributes that control water allocation priority. These are typically expressed as penalties or 'costs', so the model allocates water first to the node with the lowest penalty. If you prefer allocating by benefit, sending water to where it has the highest benefit first, you'll need to express your priorities in Pywr as negative costs (i.e., use negative numbers).  In fact, both can be used together, so for example if 3 nodes have penalties -10, 2, 6, they will get water in that order (the node with a 'penalty' of -10 gets water first, and the node with allocation penalty 6 gets water last).

## Parameter

Parameters in Pywr provide a flexible and convenient way to provide inputs to Nodes. For example, a particular parameter type can be used to load inflow or demand data from a Microsoft Excel file. Parameters also offer a flexible and customizable way to define a system's operating rules (e.g., rules governing reservoir releases). Most model input data can be provided using parameters.&#x20;

## Recorder

Pywr Recorders are used to post-process results. By creating a recorder, you can observe and save simulation results. Some recorders enable aggregating results over time (e.g., from daily to annual) and space (e.g., water allocated to a group of nodes).

## Scenario

In Pywr you can create and simulate scenarios with different input data on supply, demand or other changes. Water planners increasingly use long-term simulations with many scenarios to evaluate future changes or test possible interventions. Being able to quickly simulate many plausible future scenarios is one of Pywr's main benefits.



_**Note:**_

For further details, please refer to the open-access paper entitled: [A water resource simulator in Python](https://doi.org/10.1016/j.envsoft.2020.104635).
