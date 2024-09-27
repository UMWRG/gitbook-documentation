# Array Indexed Scenario Monthly Factors

## General Description

Time varying parameter using an array and Timestep.index with multiplicative factors per Scenario.

Values is the baseline timeseries data that is perturbed by a factor. The factor is taken from factors which is shape (scenario.size, 12). Therefore factors vary with the individual scenarios in scenario and month. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.ArrayIndexedScenarioMonthlyFactorsParameter.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="409">Description</th><th>Required</th></tr></thead><tbody><tr><td>scenario</td><td>Scenario object over which different profiles should be provided</td><td>Yes</td></tr><tr><td>values</td><td>Length of 1st dimension should equal the number of members in the scenario object and the length of the second dimension should be 12</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
