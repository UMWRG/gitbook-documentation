# Minimum Threshold Volume Storage Recorder

## General Description

Record whether a _Storage_ node falls below a particular volume threshold during a simulation.

This recorder will return a value of _1.0_ for scenarios where the volume _Storage_ is less than or equal to the threshold at any time-step during the simulation. Otherwise it will return zero. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.MinimumThresholdVolumeStorageRecorder.html)

## Attributes

<table><thead><tr><th width="155">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>pywr.core.Model</td><td>Optional</td></tr><tr><td>node</td><td>The node to record</td><td>Required</td></tr><tr><td>name</td><td>The name of the recorder</td><td>Optional</td></tr><tr><td>threshold</td><td>The threshold to compare the parameter to</td><td>Optional</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
