# Mean Parameter Recorder

## General Description

Record the mean value of a _Parameter_ during a simulation.

This recorder can be used to track the mean of the values returned by a _Parameter_ during a models simulation. An optional factor can be provided to apply a linear scaling of the values. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.MeanParameterRecorder.html)

## Attributes

<table><thead><tr><th width="155">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.core.Model</td><td>Optional</td></tr><tr><td>name</td><td>The name of the recorder</td><td>Optional</td></tr><tr><td>param</td><td>The parameter to record</td><td>Required</td></tr><tr><td>factor</td><td>Scaling factor for the values of <em>param</em></td><td>Optional</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
