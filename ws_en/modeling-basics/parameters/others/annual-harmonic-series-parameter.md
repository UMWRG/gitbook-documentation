# Annual Harmonic Series Parameter

## General Description

A _Parameter_ which returns the value from an annual harmonic series.

This _Parameter_ comprises a series N cosine function with a period of 365 days. The calculation is performed using the Julien day of the year minus 1. This causes a small discontinuity in non-leap years. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.AnnualHarmonicSeriesParameter.html#pywr.parameters.AnnualHarmonicSeriesParameter)

$$f(t)=A+∑n=1NAn⋅cos((2πnt)/365+ϕn)$$

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>mean</td><td>Mean value for the series (i.e. the position of zeroth harmonic)</td><td>Yes</td></tr><tr><td>amplitudes</td><td>The amplitudes for the N harmonic cosine functions. Must be the same length as phases</td><td>Yes</td></tr><tr><td>phases</td><td>The phase shift of the N harmonic cosine functions. Must be the same length as amplitudes</td><td>Yes</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
