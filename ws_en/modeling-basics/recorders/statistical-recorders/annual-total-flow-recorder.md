# Annual Total Flow Recorder

## General Description

For each scenario, record the total flow in each year across a list of nodes. Output from data property has shape: (years, scenario combinations).

A list of factors can be provided to scale the total flow (e.g. for calculating operational costs).[ ](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.NumpyArrayNodeCurtailmentRatioRecorder.html)[API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.AnnualTotalFlowRecorder.html#pywr.recorders.AnnualTotalFlowRecorder)

## Attributes

<table><thead><tr><th width="155">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td></td><td></td></tr><tr><td>name</td><td>The name of the recorder</td><td>Optional</td></tr><tr><td>nodes</td><td>List of <em>pywr.core.Node</em> instances to record</td><td>Optional</td></tr><tr><td>factors</td><td>List of factors to apply to each node</td><td>Optional</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
