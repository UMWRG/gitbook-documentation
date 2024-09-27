# Piecewise Integral Parameter

## General Description

Parameter that integrates a piecewise function.

This parameter calculates the integral of a piecewise function. The piecewise function is given as two arrays (_x_ and _y_) and is assumed to start from (0, 0). The values of _x_ should be monotonically increasing and greater than zero. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.PiecewiseIntegralParameter.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>parameter</td><td>The parameter the defines the right hand bounds of the integration</td><td>Yes</td></tr><tr><td>x</td><td>iterable of doubles</td><td>Yes</td></tr><tr><td>y</td><td>iterable of doubles</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
