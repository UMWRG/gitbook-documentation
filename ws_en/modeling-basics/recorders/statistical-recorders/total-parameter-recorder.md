# Total Parameter Recorder

## General Description

Record the total value of a _Parameter_ during a simulation.

This recorder can be used to track the sum total of the values returned by a _Parameter_ during a models simulation. An optional factor can be provided to apply a linear scaling of the values. If the parameter represents a flux the _integrate_ keyword argument can be used to multiply the values by the time-step length in days. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.TotalParameterRecorder.html)

## Attributes

<table><thead><tr><th width="155">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.core.Model</td><td>Optional</td></tr><tr><td>param</td><td>The parameter to record</td><td>Required</td></tr><tr><td>name</td><td>The name of the recorder</td><td>Optional</td></tr><tr><td>factor</td><td>Scaling factor for the values of <em>param</em></td><td>Optional</td></tr><tr><td>integrate</td><td>Whether to multiply by the time-step length in days during summation</td><td>Optional</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
