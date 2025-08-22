---
layout: default
title: "Wildfires and power grid"
permalink: /wildfires/
---

# Wildfire impact on power grids - California test cases

We intersect wildfire paths (both realtime probabilistic forecasts and historical data) with power grids and build contingencies: which grid components (lines, transformers, generators, and loads) are inoperable due to the wildfire. These are known as N-k contingencies, and generally, the number k of grid elements inoperable is quite large. Nonlinear  N-k security-constrained ACOPF (SC-ACOPF) models are used to optimally and safely position the grid with respect to these contingencies. Test cases are using the California test system (CATS) and California wildfire path predictions and historical data. 


## Monument wildfire
The Monument wildfire occurred west of Big Bar in the Shasta-Trinity National Forest, Trinity County. This fire ignited on July 30, 2021, and was contained on October 27, 2021, ultimately burning 223,124 acres.

For our simulation, we used historical wildfire data to model potential impacts on power infrastructure. From this data, we needed to define a safe distance (SD) zone within which the wildfire could potentially affect electrical equipment. Within this designated zone, all power lines, transformers, and generators are marked as inoperable as a safety precaution. Given that this fire occurred during summer conditions in a forested area, we took SD to be 12 miles. As a result, our analysis identified that 25 power lines, 4 transformers, and 1 generator would need to be deactivated during the fire event.

<!--
SD: 6
Number of off lines: 16
Number of off transformers: 3
Number of off generator buses: 0

SD: 2
Number of off lines: 4
Number of off transformers: 0
Number of off generator buses: 0
-->

Interactive map of CATS and wildfires, together with the minimally disrupted CATS power flows found by our methodology is shown <a href="{{ site.baseurl }}/wildfires/Monument_SD_12.html">here</a>.

## Eaton fire
The Eaton wildfire occurred in Los Angeles County, Southern California. The fire began on January 7, 2025, and was contained on January 31, 2025, ultimately burning 14,021 acres. This was one of several major fires occurring simultaneously in the region.

For our simulation, we used probabilistic forecasted data to model the potential impacts on electrical infrastructure. Given the urban setting of this fire, we established an SD zone of only 2 miles from the fire perimeter, as the urban environment reduces the likelihood of fire spread compared to forested areas. Based on the choice of SD, our analysis identified that 92 power lines, 4 transformers, and 13 generators would need to be deactivated during the fire event.


Interactive map of CATS and wildfires, together with the minimal disrupted CATS power flows found by our methodology is shown <a href="{{ site.baseurl }}/wildfires/Eaton_50p_SD_2.html">here</a>.

## Stress test - multiple wildfires
For the stress test, we ran our simulation with multiple wildfires occurring simultaneously. We collected data from the major wildfires that occurred in Southern California during January 2025, specifically the Palisades, Eaton, Kenneth, and Hurst wildfires. Each fire was assigned an SD zone of 2 miles, reflecting the urban environment common to all these fire locations.
Our analysis identified that 97 power lines, 7 transformers, and 14 generators would need to be deactivated during the concurrent wildfire events. The deactivation of these power lines and transformers created four separate electrical islands within the grid system. This extreme scenario with multiple contingencies and islanding conditions severely stress tested our numerical and modeling optimization techniques.
To achieve robust optimization and numerical convergence under this extreme setup, we employed several advanced modeling techniques, including slack real and reactive power variables with smooth convex penalties and voltage regularizations. We also used specialized numerical optimization methods such as dual regularizations and carefully chosen starting points. These techniques enabled our SC-ACOPF algorithm to converge successfully despite the challenging conditions.

Interactive map of CATS and wildfires, together with the minimally disruptive power flows found by our methodology is shown <a href="{{ site.baseurl }}/wildfires/islands_reduced.html">here</a>.