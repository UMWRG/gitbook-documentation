# Interpolated Quadrature

## General Description

Parameter value is equal to the quadrature of the interpolation of another parameter.[ API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.InterpolatedQuadratureParameter.html)

## Attributes

<table><thead><tr><th width="178">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>upper_parameter</td><td>Upper value of the interpolated interval to integrate over</td><td>Yes</td></tr><tr><td>x</td><td>x coordinates of the data points for interpolation</td><td>Optional</td></tr><tr><td>y</td><td>y coordinates of the data points for interpolation</td><td>Optional</td></tr><tr><td>lower_parameter</td><td>Lower value of the interpolated interval to integrate over. Can be <em>None</em> in which case the lower value of interval is zero</td><td>Optional</td></tr><tr><td>interp_kwargs</td><td>Dictionary of keyword arguments to pass to <em>scipy.interpolate.interp1d</em> class and used for interpolation</td><td>Optional</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
