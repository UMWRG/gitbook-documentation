# Scenario Wrapper Parameter

## General Description

Parameter that utilises a different child parameter in each scenario ensemble.

This parameter is used to switch between different child parameters based on different ensembles in a given _Scenario_. It can be used to vary data in a non-scenario aware parameter type across multiple scenario ensembles. For example, many of control curve or interpolation parameters do not explicitly support scenarios. This parameter can be used to test multiple control curve definitions as part of a single simulation. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.ScenarioWrapperParameter.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>scenario</td><td>The scenario instance which is used to select the parameters</td><td>Yes</td></tr><tr><td>parameters</td><td>The child parameters that are used in each of <em>scenario</em>’s ensembles. The number of parameters must equal the size of the given scenario</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
