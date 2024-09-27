# Annual Count Index Threshold Recorder

## General Description

For each scenario, count the number of times a list of parameters exceeds a threshold in each year. If multiple parameters exceed in one timestep then it is only counted once.

Output from data property has shape: (years, scenario combinations). [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.AnnualCountIndexThresholdRecorder.html)

## Attributes

<table><thead><tr><th width="175">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.core.Model</td><td>Optional</td></tr><tr><td>parameters</td><td>List of <em>pywr.core.IndexParameter</em> to record against</td><td>Required</td></tr><tr><td>name</td><td>The name of the recorder</td><td>Optional</td></tr><tr><td>threshold</td><td>Threshold to compare parameters against</td><td>Optional</td></tr><tr><td>exclude_months</td><td>Optional list of month numbers to exclude from the count</td><td>Optional</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
