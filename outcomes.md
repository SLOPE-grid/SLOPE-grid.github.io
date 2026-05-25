---
layout: default
title: "Outcomes"
permalink: /outcomes/
---

# Highlights of project output   


## Submitted manuscript
I. Romero, N. Chiang, I. Aravena, R. Marcia, N. Petra, JP. Watson, C. G. Petra, <i>Wildfire-driven N-k contingency generation for security-constrained AC optimal power flow in the California power grid</i>, submitted, 2026. <a href="{{ site.baseurl }}/romero_wildfire.pdf">PDF.</a>

## Submitted manuscript
C. G. Petra, <i> A Proximal Oracle Sequential NLP Algorithm for Constrained Nonsmooth Optimization</i>, 2026. <a href="{{ site.baseurl }}/petra_proxsnlp_long.pdf">PDF.</a>

## Accepted paper

T. Su, J. Zhao, E. M. Constantinescu, C. G. Petra, <i>Multi-Fidelity Dynamic Line Rating Fusion for System Load Margin Enhancement with Large-Scale Offshore Wind Generations </i>, IEEE Transactions on Power Systems, online, 2026. <a href="https://ieeexplore.ieee.org/document/11483335"> DOI </a>.

## Power grid short-term response to wildfires 
<div style="text-align: center;">
<a href="{{ site.baseurl }}/wildfires/">
  <img src="{{ site.baseurl }}/wildfires/four_wildfires_pic.png" alt="4 concurent California wildfires">
</a>
</div>
We developed capabilities that intersect wildfire paths (both realtime probabilistic forecasts and historical data) with power grids. This allows  detecting grid components that may be affected by wildfire and building a list of N-k contingencies. Nonlinear  N-k security-constrained ACOPF models are used to optimally and safely position the grid with respect to this contingencies. Test cases using California test system and California wildfires are available <a href="{{ site.baseurl }}/wildfires/">here</a>.

## <a href="https://github.com/LLNL/exajugo">ExaJuGO</a>: a Julia library for SC-ACOPF 

## <a href="https://github.com/SLOPE-grid/tsSLOPE">tsSLOPE</a> 
tsSLOPE integrates learning models for transient stability into  ACOPF models for simultaneous optimization via interior-point algorithms and automatic differentiation.