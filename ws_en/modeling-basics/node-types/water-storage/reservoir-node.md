# Reservoir Node

## General Description

The **reservoir node** is a subclass of storage node with additional functionality to represent evaporation and precipitation. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.domains.river.Reservoir.html).



## Primary Attributes

<table><thead><tr><th width="180.33333333333331">Name</th><th width="316">Description</th><th>Required</th></tr></thead><tbody><tr><td>allocation penalty</td><td>The cost per unit flow via the node</td><td>Optional</td></tr><tr><td>min_volume</td><td>The minimum volume of the storage. Defaults to 0.0</td><td>Optional</td></tr><tr><td>max_volume</td><td>The maximum volume of the storage. Defaults to 0.0</td><td>Required, otherwise defaults to 0</td></tr><tr><td>initial_volume, initial_volume_pc</td><td>Specify initial volume in either absolute or proportional terms. Both are required if <em>max_volume</em> is a parameter because the parameter will not be evaluated at the first time-step. If both are given and <em>max_volume</em> is not a Parameter, then the absolute value is ignored</td><td>One is required</td></tr><tr><td>area, level</td><td>Optional float or Parameter defining the area and level of the storage node. These values are accessible through the <em>get_area</em> and <em>get_level</em> methods respectively</td><td>Optional</td></tr><tr><td>evaporation, precipitation</td><td>Evaporation and precipitation rates (length/day)</td><td>Optional</td></tr><tr><td>unit_conversion</td><td>Conversion factor to convert precipitation and evaporation to required length/day units</td><td>Optional, default is 0.001 to convert mm/day for use with km2 reservoir area</td></tr><tr><td>evaporation penalty (evaporation cost)</td><td>Allocation penalty set on the evaporation output </td><td>Optional, defaults to -999</td></tr></tbody></table>



## Examples

coming soon...
