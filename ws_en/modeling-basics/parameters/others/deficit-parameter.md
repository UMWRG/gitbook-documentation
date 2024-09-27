# Deficit Parameter

## General Description

Parameter track the deficit (max\_flow - actual flow) of a Node. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.DeficitParameter.html)

Notes: This parameter is a little unusual in that it’s value is calculated during the after method, not calc\_values. It is intended to be used in combination with a recorder (e.g. NumpyArrayNodeRecorder) to record the deficit ( defined as requested - actual flow) at a node. Note that this means recording this parameter does _not_ give you the value that was used by the solver in this timestep. Alternatively, this parameter can be used in the model by other parameters and will evaluate to _yesterdays_ deficit, where the deficit in the zeroth timestep is zero.

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.model.Model</td><td>Yes</td></tr><tr><td>node</td><td>The node that will have it’s deficit tracked</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
