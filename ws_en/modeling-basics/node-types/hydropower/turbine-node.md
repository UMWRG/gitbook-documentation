# Turbine Node

## General Description

The **turbine node** can represent a turbine of a hydropower station. It calculates the flow required to generate a particular hydropower production target in each time step. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.HydropowerTargetParameter.html).



## Primary Attributes

<table><thead><tr><th width="180.33333333333331">Name</th><th width="316">Description</th><th>Required</th></tr></thead><tbody><tr><td>allocation penalty</td><td>The cost per unit flow via the node</td><td>Optional</td></tr><tr><td>target</td><td>Hydropower production target. Units should be in units of energy per day</td><td>Optional</td></tr><tr><td>water_elevation_parameter</td><td>Elevation of water entering the turbine. The difference of this value with the <em>turbine_elevation</em> gives the working head of the turbine</td><td>Optional</td></tr><tr><td>max_flow</td><td>Upper bounds on the calculated flow. If set the flow returned by this parameter is at most the value of the max_flow parameter</td><td>Optional</td></tr><tr><td>min_flow</td><td>Lower bounds on the calculated flow. If set the flow returned by this parameter is at least the value of the min_flow parameter</td><td>Optional</td></tr><tr><td>min_head</td><td>Minimum head for flow to occur. If actual head is less than this value zero flow is returned</td><td>Optional</td></tr><tr><td>turbine_elevation</td><td>Elevation of the turbine itself. The difference between the <em>water_elevation</em> and this value gives the working head of the turbine</td><td>Optional</td></tr><tr><td>efficiency</td><td>The efficiency of the turbine</td><td>Optional</td></tr><tr><td>density</td><td>The density of water</td><td>Optional</td></tr><tr><td>flow_unit_conversion</td><td>A factor used to transform the units of flow to be compatible with the equation here. This should convert flow to units of m3/day<br></td><td>Optional</td></tr><tr><td>energy_unit_conversion</td><td>A factor used to transform the units of total energy. Defaults to 1e-6 to return MJ</td><td>Optional</td></tr></tbody></table>



## Examples

coming soon...
