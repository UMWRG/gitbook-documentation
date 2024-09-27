# Abstract Threshold

## General Description

Base class for parameters returning one of two values depending on other state. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.AbstractThresholdParameter.html#pywr.parameters.AbstractThresholdParameter)

## Attributes

<table><thead><tr><th width="187">Name</th><th width="409">Description</th><th>Required</th></tr></thead><tbody><tr><td>threshold</td><td>Threshold to compare the value of the recorder to</td><td>Yes</td></tr><tr><td>values</td><td>If the predicate evaluates False the zeroth value is returned, otherwise the first value is returned</td><td>Yes</td></tr><tr><td>predicate</td><td>One of {“LT”, “GT”, “EQ”, “LE”, “GE”}</td><td>Yes</td></tr><tr><td>ratchet</td><td>If true the parameter behaves like a ratchet. Once it is triggered first it stays in the triggered position (default=False)</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
