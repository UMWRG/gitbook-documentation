# Storage Threshold

## General Description

Returns one of two values depending on current volume in a Storage node. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.StorageThresholdParameter.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="409">Description</th><th>Required</th></tr></thead><tbody><tr><td>threshold</td><td>Threshold to compare the value of the recorder to</td><td>Yes</td></tr><tr><td>storage</td><td>storage: pywr._core.AbstractStorage</td><td>Yes</td></tr><tr><td>ratchet</td><td>If true the parameter behaves like a ratchet. Once it is triggered first it stays in the triggered position (default=False)</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```