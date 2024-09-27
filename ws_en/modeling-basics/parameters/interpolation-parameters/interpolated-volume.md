# Interpolated Volume

## General Description

Generic interpolation parameter that returns a value based on a Reservoir or Storage nodes current (time step) volume. The

&#x20;parameter uses an **array** (table) of **Reservoir Volumes** and corresponding values. In this case the associated values are the corresponding **Reservoir Area** for a given **Volume**.&#x20;

Interpolation is used to calculate values betwen points given in the interpolation array. [ API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.InterpolatedVolumeParameter.html#pywr.parameters.InterpolatedVolumeParameter)

## Attributes

<table><thead><tr><th width="167">Name</th><th width="392">Description</th><th>Required</th></tr></thead><tbody><tr><td>type</td><td>interpolatedvolume</td><td>Yes</td></tr><tr><td>node</td><td>Storage node to provide input volume values to interpolation calculation</td><td>Yes</td></tr><tr><td>volumes</td><td>x coordinates of the data points for interpolation</td><td>Yes</td></tr><tr><td>values</td><td>y coordinates of the data points for interpolation</td><td>Yes</td></tr><tr><td>interp_kwargs</td><td>Dictionary of keyword arguments to pass to <em>scipy.interpolate.interp1d</em> class and used for interpolation</td><td>Optional</td></tr></tbody></table>

## Example

The following Json shows an example Area vs Volume rating cure for a reservoir. This could be used to define the Area attribute of a Storage or Reservoir node.

```json
{
  "type": "InterpolatedVolumeParameter",
  "node": "Reservoir or Storage node name",
	"volumes": [
		0,
		7,
		10,
		15,
		25
	],
	"values": [
		1,
		2,
		4,
		6,
		14
	],

	"interp_kwargs": {
		"kind": "linear"
	},
  "comment": "volumes: Mm3, values:  Km2"
}
```

The Json represents the table below:

<table><thead><tr><th width="166">Volume (Mm3)</th><th width="182">Area (Km2)</th></tr></thead><tbody><tr><td>0</td><td>1</td></tr><tr><td>7</td><td>2</td></tr><tr><td>10</td><td>4</td></tr><tr><td>15</td><td>6</td></tr><tr><td>25</td><td>14</td></tr></tbody></table>

When plotted it looks like this:

Below is an example Area rating table

<table><thead><tr><th width="166">Volume (Mm3)</th><th width="182">Area (Km2)</th></tr></thead><tbody><tr><td>0</td><td>1</td></tr><tr><td>7</td><td>2</td></tr><tr><td>10</td><td>4</td></tr><tr><td>15</td><td>6</td></tr><tr><td>25</td><td>14</td></tr></tbody></table>

When plotted it looks like this

<figure><img src="../../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>
