# RBF Profile

## General Description

Parameter which interpolates a daily profile using a radial basis function (RBF).

The daily profile is computed during model _reset_ using a radial basis function with day-of-year as the independent variables. The days of the year are defined by the user alongside the values to use on each of those days for the interpolation. The first day of the years should always be one, and its value is repeated as the 366th value. In addition the second and penultimate values are mirrored to encourage a consistent gradient to appear across the boundary. The RBF calculations are undertaken using the _scipy.interpolate.Rbf_ object, please refer to Scipy’s documentation for more information. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.RbfProfileParameter.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="409">Description</th><th>Required</th></tr></thead><tbody><tr><td>days_of_year</td><td>The days of the year at which the interpolation values are defined. The first value should be one</td><td>Yes</td></tr><tr><td>values</td><td>Values to use for interpolation corresponding to the <em>days_of_year</em></td><td>Yes</td></tr><tr><td>lower_bounds</td><td>The lower bounds of the values when used during optimisation</td><td>Yes</td></tr><tr><td>upper_bounds</td><td>The upper bounds of the values when used during optimisation</td><td>Yes</td></tr><tr><td>variable_days_of_year_range</td><td>The maximum bounds (positive or negative) for the days of year during optimisation. A non-zero value will cause the days of the year values to be exposed as integer variables (except the first value which remains at day 1). This value is bounds on those variables as maximum shift from the given <em>days_of_year</em></td><td>Yes</td></tr><tr><td>min_value, max_value</td><td>Optionally cap the interpolated daily profile to a minimum and/or maximum value. The default values are negative and positive infinity for minimum and maximum respectively</td><td>Yes</td></tr><tr><td>rbf_kwargs</td><td>Optional dictionary of keyword arguments to base to the Rbf object</td><td>Optional</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
