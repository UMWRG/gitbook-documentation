# Scenario Daily Profile

## General Description

Parameter which provides a daily profile per scenario.

This parameter provides a repeating annual profile with a daily resolution. A different profile is returned for each member of a given scenario. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.ScenarioDailyProfileParameter.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="409">Description</th><th>Required</th></tr></thead><tbody><tr><td>scenario</td><td>Scenario object over which different profiles should be provided</td><td>Yes</td></tr><tr><td>values</td><td>Length of 1st dimension should equal the number of members in the scenario object and the length of the second dimension should be 366</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
