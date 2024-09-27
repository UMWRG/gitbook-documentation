---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Background on Evaporation and Precipitation on Reservoirs

## Quantifying Evaporation and Precipitation flow <a href="#quantifying-evaporation-and-precipitation-flow" id="quantifying-evaporation-and-precipitation-flow"></a>

**Evaporation losses** and added storage via **precipitation** are major components of a reservoir's mass balance. Evaporation and precipitation rates are both generally measured in length/time. In metric units this is often **mm/day**.

To get volumetric daily flow rates which are required for Pywr, these rates are then multiplied by the **Area** of the reservoir. In the metric templates in WaterStrategy this Area is generally expressed in **Km2**.

**For a template that uses flow in **<mark style="color:purple;">**Mm3/day**</mark>**, a conversion of 0.001 is required to obtain **<mark style="color:purple;">**Mm3/day**</mark>**.**

_Evaporation (mm/day) \* Area (km) \* 0.001 = Mm3/day_

**For a template that uses flow in Ml/day, no conversion is required to obtain Ml/day.**

_Evaporation (mm/day) \* Area (km) \* 1 = Ml/day_
