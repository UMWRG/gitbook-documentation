# Total Hydro Energy Recorder

## General Description

Calculates the total energy production using the hydropower equation from a model run.

This recorder saves the total energy production in each scenario during a model run. It does not save a timeseries or power, but rather total energy. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.recorders.TotalHydroEnergyRecorder.html)

## Attributes

<table><thead><tr><th width="175">Name</th><th width="395">Description</th><th>Required</th></tr></thead><tbody><tr><td>water_elevation_parameter</td><td>Elevation of water entering the turbine. The difference of this value with the <em>turbine_elevation</em> gives the working head of the turbine</td><td>Required</td></tr><tr><td>turbine_elevation</td><td>Elevation of the turbine itself. The difference between the <em>water_elevation</em> and this value gives the working head of the turbine</td><td>Required</td></tr><tr><td>efficiency</td><td>The efficiency of the turbine</td><td>Optional</td></tr><tr><td>density</td><td>The density of water</td><td>Optional</td></tr><tr><td>flow_unit_conversion</td><td>A factor used to transform the units of flow to be compatible with the equation here. This should convert flow to units of <span class="math">m3/day</span></td><td>Optional</td></tr><tr><td>energy_unit_conversion</td><td>A factor used to transform the units of total energy. Defaults to 1e-6 to return <span class="math">MJ</span></td><td>Optional</td></tr></tbody></table>

## Example

coming soon...

```json
{

}
```
