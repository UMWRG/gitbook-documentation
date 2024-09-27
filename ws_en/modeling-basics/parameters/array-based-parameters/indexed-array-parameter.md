# Indexed Array Parameter

## General Description

Parameter which uses an IndexParameter to index an array of Parameters.

An example use of this parameter is to return a demand saving factor (as a float) based on the current demand saving level (calculated by an _IndexParameter_). [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.IndexedArrayParameter.html#pywr.parameters.IndexedArrayParameter)

## Attributes

<table><thead><tr><th width="158">Name</th><th width="409">Description</th><th>Required</th></tr></thead><tbody><tr><td>index_parameter</td><td>IndexParameter</td><td>Yes</td></tr><tr><td>params</td><td>iterable of <em>Parameters</em> or floats</td><td>Yes</td></tr></tbody></table>

## Example

```
{
	"type": "indexedarrayparameter",
	"index_parameter": "Reservoir control curve",
	"params": [
		1,
		0.9,
		0.8,
		0.5
	]
}

```

The above code uses the Index supplied by the parameter called 'Reservoir control curve', which is a [Control Curve Index Parameter.](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/control-curve-index-parameter) Index 0 returns a 1, Index 2 returns 0.9 etc...

In this example this parameter is used to reduce a demand based on a reservoir control curve. Please go to the [Aggregated Parameter example](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/aggregated-parameter#example) to see how this is done.

Please see how the Reservoir control curve parameter is defined.
