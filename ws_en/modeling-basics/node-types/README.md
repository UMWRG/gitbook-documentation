# Node Types

This table introduces the most commonly used Pywr node types:

<table><thead><tr><th width="186">Node Type</th><th width="159">Icon</th><th>Brief Description</th></tr></thead><tbody><tr><td>Input Node</td><td><img src="../../.gitbook/assets/image (292).png" alt="" data-size="line"></td><td>Input nodes represent water inputs into the system.</td></tr><tr><td>Catchment Node</td><td><img src="../../.gitbook/assets/image (274).png" alt="" data-size="line"></td><td>Catchment nodes are often used to represent river or other type of inflow into the system.</td></tr><tr><td>Proportional Input Node</td><td><img src="../../.gitbook/assets/image (285).png" alt="" data-size="original"></td><td>Proportional input node is intended for a simple case of where fixed ratio of flow is required to be distributed to multiple downstream routes.</td></tr><tr><td>Link Node</td><td><img src="../../.gitbook/assets/image (286).png" alt="" data-size="line"></td><td>Link node represents a link in the water system or other point of interest where a maximum or minimum flow constraint or an allocation priority are assigned.</td></tr><tr><td>River Node</td><td><img src="../../.gitbook/assets/image (295).png" alt="" data-size="line"></td><td>River node is a node in the river network, which may have multiple upstream nodes (i.e. a confluence) but only one downstream node.</td></tr><tr><td>Delay Node</td><td><img src="../../.gitbook/assets/image (278).png" alt="" data-size="line"></td><td>These delay flow for a given number of timesteps or days. This is used when flow propagation time cannot be ignored, for example because time-steps are relatively short.</td></tr><tr><td>Storage Node</td><td><img src="../../.gitbook/assets/image (279).png" alt="" data-size="line"></td><td>Storage node is a general node that can store water (like dams or aquifers), which have a minimum and maximum volume restrictions.</td></tr><tr><td>Reservoir Node</td><td><img src="../../.gitbook/assets/image (291).png" alt="" data-size="line"></td><td>Reservoir node is a type of storage node with additional functionality to represent evaporation and precipitation.</td></tr><tr><td>Output Node</td><td><img src="../../.gitbook/assets/image (281).png" alt="" data-size="line"></td><td>Output nodes are locations where water leaves the system.</td></tr><tr><td>Loss Link Node</td><td><img src="../../.gitbook/assets/image (290).png" alt="" data-size="line"></td><td>Loss link allows for the definition of a fixed proportional loss of flow that goes through this node.</td></tr><tr><td>Turbine Node</td><td><img src="../../.gitbook/assets/image (288).png" alt="" data-size="line"></td><td>Turbine node can represent a turbine of a hydropower station. It calculates the flow required to generate a particular hydropower production target in each time step.</td></tr></tbody></table>

Pywr Node types can also be further sub-divided into 6 categories: [Water Input](https://water-strategy.gitbook.io/water-strategy/modeling-basics/node-types/water-input), [Water Transport](https://water-strategy.gitbook.io/water-strategy/modeling-basics/node-types/water-transport), [Water Storage](https://water-strategy.gitbook.io/water-strategy/modeling-basics/node-types/water-storage), [Water Output](https://water-strategy.gitbook.io/water-strategy/modeling-basics/node-types/water-output), [Hydropower](https://water-strategy.gitbook.io/water-strategy/modeling-basics/node-types/hydropower), and [Others](https://water-strategy.gitbook.io/water-strategy/modeling-basics/node-types/others). You can find more details about these groupings of nodes and nodes types in the sub-sections of the 'Node Types' section.

## More details

An overview of nodes in Pywr can be found [here](https://pywr.github.io/pywr-docs/master/json.html#nodes.).  The full list of built-in nodes in Pywr can be found [here](https://pywr.github.io/pywr-docs/master/api/pywr.nodes.html).