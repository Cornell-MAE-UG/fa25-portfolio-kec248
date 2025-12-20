---
layout: project
title: Thermo Heat Exchanger
description: Advanced CAD Project
technologies: [Autodesk Fusion]
image: /assets/images/heat_exchnager_setup.jpg
---

<h1>Heat Exchanger Setup</h1>

This project investigates a heat exchanger used to transfer thermal energy between two separate fluid streams (hot and cold) without mixing. The primary objectives are to measure the heat transfer rate for both parallel-flow and counterflow arrangements, calculate the overall heat transfer coefficient, and compare experimental results to theoretical predictions. Hot water is circulated from a heated reservoir and cold water from a chilled reservoir; the fluids remain separated by the exchanger wall and exchange heat via conduction through the wall and convection at the fluid interfaces.

Lab Measurements and Data: inlet and outlet temperatures for each stream and mass flow rates. From the measured values we compute the heat transfer rate and the entropy generation.

These results are used to determine the overall heat transfer and the effectiveness of the exchanger, and to discuss sources of error and heat loss in the setup.


<h2>Parallel Flow (Control Group)</h2>

<p>
  In the parallel-flow configuration, both the hot and cold fluids enter the heat exchanger at the
  same end and flow in the same direction. As the fluids travel together, the temperature difference
  between them decreases rapidly, which limits the overall heat-transfer effectiveness and results
  in smaller temperature changes.
</p>

<p>
  <strong>Hot reservoir:</strong> 43.1&nbsp;°C → 27.3&nbsp;°C<br>
  <strong>Cold reservoir:</strong> 4.0&nbsp;°C → 23.6&nbsp;°C
</p>

<p>
  <strong>Observations:</strong><br>
  During parallel flow, uneven heating was observed in the metal pump block. The 2/4 side of the pump
  consistently became hotter than the 1/3 side associated with the cold flow. This indicates
  nonuniform heat distribution and suggests that the heat exchanger is not perfectly insulated,
  with some heat either lost to the surroundings or unevenly conducted through the metal block.
</p>

<h2>Counterflow Configuration</h2>

<p>
  In the counterflow configuration, the hot and cold fluids flow in opposite directions through the
  heat exchanger. This arrangement maintains a larger temperature difference along the entire
  length of the exchanger, resulting in significantly higher thermal effectiveness and increased
  heat transfer.
</p>

<p>
  <strong>Hot reservoir:</strong> 43.1&nbsp;°C → 23.0&nbsp;°C<br>
  <strong>Cold reservoir:</strong> 6.3&nbsp;°C → 28.1&nbsp;°C
</p>

<p>
  <strong>Observations:</strong><br>
  Shortly after flow initiation, the hot reservoir temperature increased to approximately 44.5&nbsp;°C
  before decreasing. The cold reservoir outlet temperature exceeded the hot reservoir outlet
  temperature, while the hot stream exited at a lower temperature than the cold stream. This
  temperature crossover is only possible in a counterflow heat exchanger and demonstrates its
  higher effectiveness compared to parallel flow.
</p>

<h2>Parallel Flow with Higher Hot Inlet Temperature</h2>

<p>
  This trial repeated the parallel-flow configuration with an increased hot inlet temperature.
  Increasing the hot inlet temperature raises the initial driving temperature difference, which
  is expected to increase the heat-transfer rate.
</p>

<p>
  <strong>Hot reservoir:</strong> 50.0&nbsp;°C → 30.0&nbsp;°C<br>
  <strong>Cold reservoir:</strong> 4.0&nbsp;°C → 23.0&nbsp;°C
</p>

<p>
  <strong>Observations:</strong><br>
  Increasing the initial hot reservoir temperature increased the overall temperature driving force,
  but did not produce significant changes in heat exchanger behavior compared to the baseline
  parallel-flow case.
</p>

<h2>Effect of Relative Flow Rate (Reduced Hot-Side Flow Rate)</h2>

<p>
  In this experiment, the hot-side tubing was pinched to reduce the hot-side mass flow rate while
  maintaining approximately the same cold-side flow rate. The stream with the lower mass flow
  rate experiences a larger temperature change and becomes the limiting stream in the heat
  transfer process.
</p>

<p>
  <strong>Hot reservoir:</strong> 42.4&nbsp;°C → 26.5&nbsp;°C<br>
  <strong>Cold reservoir:</strong> 9.6&nbsp;°C → 24.9&nbsp;°C
</p>

<p>
  <strong>Observations:</strong><br>
  Significantly less hot fluid was present in the hot-side tubing compared to the cold side.
  The reduced hot-side mass flow resulted in a larger temperature drop in the hot stream in order
  to transfer sufficient thermal energy to the cold stream.
</p>

