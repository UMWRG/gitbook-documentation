# Interpolated Flow

## General Description

Generic interpolation parameter that uses a node’s flow at the previous time-step for interpolation.[ API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.InterpolatedFlowParameter.html)

## Attributes

<table><thead><tr><th width="154">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>type</td><td>interpolatedflow</td><td>Yes</td></tr><tr><td>node</td><td>Node to provide input flow values to interpolation calculation</td><td>Optional</td></tr><tr><td>flows</td><td>x coordinates of the data points for interpolation</td><td>Optional</td></tr><tr><td>values</td><td>y coordinates of the data points for interpolation</td><td>Optional</td></tr><tr><td>interp_kwargs</td><td>Dictionary of keyword arguments to pass to <em>scipy.interpolate.interp1d</em> class and used for interpolation</td><td>Optional</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
