# Uniform Drawdown Profile

## General Description

Parameter which provides a uniformly reducing value from one to zero.&#x20;

This parameter is intended to be used with an _AnnualVirtualStorage_ node to provide a profile that represents perfect average utilisation of the annual volume. It returns a value of 1 on the reset day, and subsequently reduces by 1/366 every day afterward. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.UniformDrawdownProfileParameter.html#pywr.parameters.UniformDrawdownProfileParameter)

## Attributes

<table><thead><tr><th width="176">Name</th><th width="390">Description</th><th>Required</th></tr></thead><tbody><tr><td>reset_day</td><td>The day of the month (1-31) to reset the volume to the initial value</td><td>Yes</td></tr><tr><td>reset_month</td><td>The month of the year (1-12) to reset the volume to the initial value</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
