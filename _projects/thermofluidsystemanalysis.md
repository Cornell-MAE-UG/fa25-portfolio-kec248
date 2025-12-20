---
layout: project
title: Thermo Heat Exchanger
description: Advanced CAD Project
technologies: 
image: /assets/images/heat_exchnager_setup.jpg
---

<h1>Heat Exchanger Setup</h1>

This project investigates a heat exchanger used to transfer thermal energy between two separate fluid streams (hot and cold) without mixing. The primary objectives are to measure the heat transfer rate for both parallel-flow and counterflow arrangements, calculate the overall heat transfer coefficient, and compare experimental results to theoretical predictions. Hot water is circulated from a heated reservoir and cold water from a chilled reservoir; the fluids remain separated by the exchanger wall and exchange heat via conduction through the wall and convection at the fluid interfaces.

Lab Measurements and Data: inlet and outlet temperatures for each stream and mass flow rates. From the measured values we compute the heat transfer rate and the entropy generation.

These results are used to determine the overall heat transfer and the effectiveness of the exchanger, and to discuss sources of error and heat loss in the setup.

Disclaimer: I worked in a group of 4 to analyze this heat exchanger, where we all recorded the same observation and data (Charlotte Huber, Kathryn Moskal, and Jillian Vondell)

<h2>Parallel Flow (Control Group)</h2>

<p>
  In the parallel-flow arrangement, the hot and cold streams enter the heat exchanger from the same
  end and move in the same direction. Because both fluids warm and cool together, the temperature
  difference between them decreases rapidly along the exchanger length. This reduction in driving
  temperature limits the amount of heat that can be transferred.
</p>

<p>
  <strong>Hot reservoir:</strong> 43.1&nbsp;°C → 27.3&nbsp;°C<br>
  <strong>Cold reservoir:</strong> 4.0&nbsp;°C → 23.6&nbsp;°C
</p>

<p>
  <strong>Observations:</strong><br>
  Uneven heating of the metal pump block was observed during parallel flow operation. The side
  associated with the hot flow (ports 2/4) consistently reached higher temperatures than the
  cold-flow side (ports 1/3). This suggests nonuniform heat conduction within the metal block and
  indicates that some thermal energy may be lost to the surroundings due to imperfect insulation.
</p>

<h2>Counterflow Configuration</h2>

<p>
  For the counterflow configuration, the hot and cold fluids enter the heat exchanger from opposite
  ends and flow in opposing directions. This arrangement maintains a larger temperature difference
  across the entire length of the exchanger, increasing thermal effectiveness and allowing greater
  overall heat transfer.
</p>

<p>
  <strong>Hot reservoir:</strong> 43.1&nbsp;°C → 23.0&nbsp;°C<br>
  <strong>Cold reservoir:</strong> 6.3&nbsp;°C → 28.1&nbsp;°C
</p>

<p>
  <strong>Observations:</strong><br>
  Shortly after flow was initiated, the hot reservoir temperature briefly increased to approximately
  44.5&nbsp;°C before beginning to cool. The cold stream exited the exchanger at a higher temperature
  than the hot stream outlet, producing a temperature crossover. This behavior is unique to
  counterflow heat exchangers and highlights their superior thermal performance compared to
  parallel-flow systems.
</p>

<h2>Parallel Flow with Increased Hot Inlet Temperature</h2>

<p>
  This trial repeated the parallel-flow configuration with a higher initial hot reservoir
  temperature. Increasing the hot inlet temperature increases the initial thermal driving force,
  which is expected to enhance the rate of heat transfer between the streams.
</p>

<p>
  <strong>Hot reservoir:</strong> 50.0&nbsp;°C → 30.0&nbsp;°C<br>
  <strong>Cold reservoir:</strong> 4.0&nbsp;°C → 23.0&nbsp;°C
</p>

<p>
  <strong>Observations:</strong><br>
  Although the higher inlet temperature increased the temperature difference between the streams,
  the overall exchanger behavior remained similar to the baseline parallel-flow case. No major
  changes in performance trends were observed.
</p>

<h2>Effect of Relative Flow Rate (Reduced Hot-Side Flow Rate)</h2>

<p>
  In this experiment, the hot-side tubing was partially constricted to reduce the hot-side mass
  flow rate while keeping the cold-side flow approximately constant. The stream with the lower mass
  flow rate experiences a larger temperature change and therefore becomes the limiting side in the
  heat transfer process.
</p>

<p>
  <strong>Hot reservoir:</strong> 42.4&nbsp;°C → 26.5&nbsp;°C<br>
  <strong>Cold reservoir:</strong> 9.6&nbsp;°C → 24.9&nbsp;°C
</p>

<p>
  <strong>Observations:</strong><br>
  The reduced hot-side flow resulted in noticeably less hot fluid within the tubing compared to the
  cold side. As a result, the hot stream underwent a larger temperature drop in order to supply
  sufficient thermal energy to the cold stream.
</p>

<h2>Actual Analysis</h2>

<p>
  The diagram shown below was used to define the control volume and establish the governing
  equations for the analysis.
</p>


<img src="{{ '/assets/images/diagram.jpg' | relative_url }}" alt="Enthalpy diagram" />

<h2>Assumptions</h2>

<ul>
  <li>The heat exchanger operates under steady-state conditions.</li>
  <li>Changes in kinetic energy and potential energy of the fluid streams are neglected.</li>
  <li>No shaft work is produced or consumed, since the device functions solely as a heat exchanger.</li>
  <li>The mass flow rate is constant, with equal inlet and outlet mass flow rates for each stream.</li>
  <li>A mass flow rate of <strong>ṁ = 0.125 kg/s</strong> is assumed for both the hot and cold streams.</li>
  <li>The working fluid is water, and inlet and outlet velocities are assumed to be the same.</li>
  <li>The specific heat capacity of water is assumed constant and equal for both streams,
      with <strong>c<sub>p</sub> = 4.18 kJ/(kg·K)</strong>.</li>
  <li>Thermophysical properties are evaluated at average fluid temperatures.</li>
</ul>

If we assumed adiabatic, we could have just used the temperatures to compare the heat exchange:
<img src="{{ '/assets/images/enthalpy.jpg' | relative_url }}" alt="Enthalpy diagram" />


<h2>Parallel Flow- Heat and Entropy Generation</h2>

<img src="{{ '/assets/images/parallel.jpg' | relative_url }}" alt="Enthalpy diagram" />


