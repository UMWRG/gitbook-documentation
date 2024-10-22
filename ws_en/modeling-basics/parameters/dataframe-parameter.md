# DataFrame Parameter

## General Description

Timeseries parameter with automatic alignment and resampling.[ API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.DataFrameParameter.html#pywr.parameters.DataFrameParameter)

## Attributes

<table><thead><tr><th width="154">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>type</td><td>dataframe</td><td>Yes</td></tr><tr><td>model</td><td></td><td>Optional</td></tr><tr><td>dataframe</td><td></td><td>Optional</td></tr><tr><td>scenario</td><td></td><td>Optional</td></tr></tbody></table>

## Example

<figure><img src="../../.gitbook/assets/image (305).png" alt="" width="375"><figcaption><p>Inflows_mm3_day.csv</p></figcaption></figure>

```json
{
	"type": "DataFrameParameter",
	"url": "Inflows_mm3_day.csv",
	"column": "Catchment River 1",
	"index_col": "timestep",
	"parse_dates": true
}
```
