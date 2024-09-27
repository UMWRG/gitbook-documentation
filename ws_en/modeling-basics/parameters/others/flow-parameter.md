# Flow Parameter

## General Description

Parameter that provides the flow from a node from the previous time-step. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.FlowParameter.html)

Notes: This parameter keeps track of the previous time step’s flow on the given node. These values can be used in calculations for the current timestep as though this was any other parameter.

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.model.Model</td><td>Yes</td></tr><tr><td>node</td><td>The node that will have its flow tracked</td><td>Yes</td></tr><tr><td>initial_value</td><td>The value to return on the first time-step before the node has any past flow</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
