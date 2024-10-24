# Control Curve Index Parameter

## Example

```
{
	"type": "controlcurveindexparameter",
	"storage_node": "Reservoir name",
	"control_curves": [
		{
			"type": "monthlyprofileparameter",
			"values": [
				0.45,
				0.45,
			  	0.45,
				0.45,
				0.45,
				0.45,
				0.45,
				0.45,
				0.45,
				0.45,
				0.6,
				0.6
				]
		},
		{
			"type": "constant",
			"value": 0.4
		},		
		{
			"type": "constant",
			"value": 0.1
		}		
	]
}

```

The above code defines 3 reservoir control curves for the reservoir called "Reservoir name". It returns an Index depending on how full the reservoir is:

<figure><img src="../../../.gitbook/assets/image (61) (1).png" alt=""><figcaption></figcaption></figure>

To see how this index is used with an[ Indexed Array Parameter ](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/indexed-array-parameter)click [here](https://water-strategy.gitbook.io/water-strategy/modelling-fundamentals/parameters/indexed-array-parameter/#Example).
