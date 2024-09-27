# Aggregated Parameter

## General Description

A collection of IndexParameters. This class behaves like a set. Parameters can be added or removed from it. It’s value is the value of it’s child parameters aggregated using a aggregating function (e.g. sum).[ API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.AggregatedParameter.html#pywr.parameters.AggregatedParameter)



## Attributes

<table><thead><tr><th width="154">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>type</td><td>aggregated</td><td>Yes</td></tr><tr><td>parameters</td><td>The parameters to aggregate</td><td>Optional</td></tr><tr><td>agg_func</td><td>The aggregation function. Must be one of {“sum”, “min”, “max”, “mean”, “product”}, or a callable function which accepts a list of values</td><td>Optional</td></tr></tbody></table>

## Example

```json
{
	"type": "AggregatedParameter",
	"agg_func": "product",
	"parameters": [
		"Baseline demand",
		"Control curve demand factor"
	]
}
```

In this case Aggregated Parameter is multipliying two parameters togther

* [Baseline demand](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/constant#example)
* Control curve demand factor

This example shows a Baseline demand being multiplied by a factor that reduces demand based on a reservoir control curve. You can click on the each of these Parameters to see how they are defined. &#x20;
