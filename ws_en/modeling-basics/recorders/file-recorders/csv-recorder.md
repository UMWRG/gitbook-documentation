# CSV Recorder

## General Description

A Recorder that saves Node values to a CSV file.

This class uses the csv package from the Python standard library. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.CSVRecorder.html#pywr.recorders.CSVRecorder)

## Attributes

<table><thead><tr><th width="175">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>model</td><td>The model to record nodes from</td><td>Optional</td></tr><tr><td>csvfile</td><td>The path to the CSV file</td><td>Required</td></tr><tr><td>scenario_index</td><td>The scenario index of the model to save</td><td>Required</td></tr><tr><td>nodes</td><td>An iterable of nodes to save data. It defaults to None which is all nodes in the model</td><td>Required</td></tr><tr><td>kwargs</td><td>Additional keyword arguments to pass to the <em>csv.writer</em> object</td><td>Optional</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
