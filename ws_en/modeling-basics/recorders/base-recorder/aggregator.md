# Aggregator

## General Description

Utility class for computing aggregate values.

Users are unlikely to use this class directly. Instead _Recorder_ sub-classes will use this functionality to aggregate their results across different dimensions (e.g. time, scenarios, etc.). [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.Aggregator.html)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="473">Description</th><th>Required</th></tr></thead><tbody><tr><td>func</td><td><p>The aggregation function to use. Can be a string or dict defining aggregation functions, or a callable custom function that performs aggregation.</p><p>When a string it can be one of: “sum”, “min”, “max”, “mean”, “median”, “product”, or “count_nonzero”. These strings map to and cause the aggregator to use the corresponding <em>numpy</em> functions.</p><p>A dict can be provided containing a “func” key, and optional “args” and “kwargs” keys. The value of “func” should be a string corresponding to the aforementioned numpy function names with the additional options of “percentile” and “percentileofscore”. These latter two functions require additional arguments (the percentile and score) to function and must be provided as the values in either the “args” or “kwargs” keys of the dictionary. Please refer to the corresponding numpy (or scipy) function definitions for documentation on these arguments.</p><p>Finally, a callable function can be given. This function must accept either a 1D or 2D numpy array as the first argument, and support the “axis” keyword as integer value that determines which axis over which the function should apply aggregation. The axis keyword is only supplied when a 2D array is given. Therefore,` the callable function should behave in a similar fashion to the numpy functions.</p></td><td>Yes</td></tr><tr><td>func_args</td><td>func_args: list</td><td>Yes</td></tr><tr><td>func_kwargs</td><td>func_kwargs: dict</td><td>Yes</td></tr></tbody></table>

## Example

```json
{
Aggregator("sum")
Aggregator({"func": "percentile", "args": [95],"kwargs": {}})
Aggregator({"func": "percentileofscore", "kwargs": {"score": 0.5, "kind": "rank"}})
}
```
