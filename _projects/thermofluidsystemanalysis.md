---
layout: project
title: Thermo Heat Exchanger
description: Thermo Project
technologies: 
image: /assets/images/heat_exchnager_setup.jpg
---

<h1>Heat Exchanger Setup</h1>

This project investigates a heat exchanger used to transfer thermal energy between two separate fluid streams (hot and cold) without mixing. The primary objectives are to measure the heat transfer rate for both parallel-flow and counterflow arrangements, calculate the overall heat transfer coefficient, and compare experimental results to theoretical predictions. Hot water is circulated from a heated reservoir and cold water from a chilled reservoir; the fluids remain separated by the exchanger wall and exchange heat via conduction through the wall and convection at the fluid interfaces.

Lab Measurements and Data: inlet and outlet temperatures for each stream and mass flow rates. From the measured values we compute the heat transfer rate and the entropy generation.

These results are used to determine the overall heat transfer and the effectiveness of the exchanger, and to discuss sources of error and heat loss in the setup.

Disclaimer: I worked in a group of 4 to analyze this heat exchanger, where we all recorded the same observation and data (Charlotte Huber, Kathryn Moskal, and Jillian Vondell)

<h2>Parallel Flow</h2>

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

<h2>Parallel Flow (Hotter Temperatures))</h2>

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


<h2>Counterflow</h2>

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

<h2>Diagrams and Calculations</h2>

<p>
  The diagram shown below was used to define the control volume and establish the governing
  equations for the analysis.
</p>


<img src="{{ '/assets/images/diagram.jpg' | relative_url }}" alt="Enthalpy diagram" style="max-width:600px;height:auto;">/>

<h2>Assumptions</h2>

<ul>
  <li>The heat exchanger operates under steady-state conditions.</li>
  <li>Changes in kinetic energy and potential energy of the fluid streams are neglected.</li>
  <li>No shaft work is produced or consumed, since the device functions solely as a heat exchanger.</li>
  <li>The mass flow rate is constant, with equal inlet and outlet mass flow rates for each stream.</li>
  <li>A mass flow rate of <strong>ṁ = 0.125 kg/s</strong> is assumed for both the hot and cold streams, due to this amazon link where we chose to use this pumps mass flow rate: https://www.amazon.com.be/-/en/Air-Pump-Up-Lift-Dehumidifiers/dp/B07D8DQMYT/ref=asc_df_B07D8DQMYT?mcid=8ea932042a543d118359cca2029b55b1&tag=begogshpadde-21&linkCode=df0&hvadid=712581418278&hvpos=&hvnetw=g&hvrand=10419331664042526324&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9219354&hvtargid=pla-519965981437&psc=1&language=en_GB&gad_source=1 </li>
  <li>The working fluid is water, and inlet and outlet velocities are assumed to be the same.</li>
  <li>The specific heat capacity of water is assumed constant and equal for both streams,
      with <strong>c<sub>p</sub> = 4.18 kJ/(kg·K)</strong>.</li>
  <li>Thermophysical properties are evaluated at average fluid temperatures.</li>
</ul>

If we assumed adiabatic, we could have just used the temperatures to compare the heat exchange:
<img src="{{ '/assets/images/enthalpy.jpg' | relative_url }}" alt="Enthalpy diagram" style="max-width:600px;height:auto;">


<h2>Calculations</h2>

Here I derive the general way of solving for these values (in this example for parallel flow), which I applied to then Parallel Flow Hotter and then Counter Flow. 

<img src="{{ '/assets/images/calculations.jpg' | relative_url }}" alt="Enthalpy diagram" style="max-width:600px;height:auto;">

<h2>Parallel Flow — Final Results</h2>

<p>
  <strong>Heat transfer rate:</strong> Q = 1.99&nbsp;kJ/s<br>
  <strong>Entropy generation rate:</strong> Ṡ<sub>gen</sub> = 0.00129&nbsp;kJ/K
</p>

<h2>Parallel Flow (Hotter Side) — Final Results</h2>

<p>
  <strong>Heat transfer rate:</strong> Q = 0.523&nbsp;kJ/s<br>
  <strong>Entropy generation rate:</strong> Ṡ<sub>gen</sub> = 0.003&nbsp;kJ/K
</p>

<h2>Counterflow — Final Results</h2>

<p>
  <strong>Heat transfer rate:</strong> Q = −0.89&nbsp;kJ/s<br>
  <strong>Entropy generation rate:</strong> Ṡ<sub>gen</sub> = 0.002&nbsp;kJ/K
</p>

<h2> Analysis </h2>

</p>
For each heat exchanger configuration, a measurable amount of heat loss to the surroundings was observed. This indicates that assuming an adiabatic system, while useful for theoretical analysis, does not always produce accurate results for real-world heat exchangers. In practice, some heat is inevitably lost to the environment.

The observed heat loss can be attributed in part to conduction through the metal walls of the heat exchanger and subsequent heat transfer to the surrounding air, as the exchanger is not perfectly insulated. These losses reduce the amount of thermal energy transferred between the fluid streams.

Additionally, the parallel flow heat exchanger experienced greater heat loss than the counterflow. In parallel flow, the temperature difference between the hot and cold fluids decreases rapidly along the exchanger length, reducing internal heat transfer effectiveness and allowing a larger fraction of the thermal energy to escape to the surroundings. Counterflow maintains a more uniform temperature difference, which promotes more effective internal heat transfer and reduces external losses.

Non-uniform flow distribution may have also contributed to experimental error. Because the water reservoir was not actively stirred while heat was added, some regions of the fluid may have been at different temperatures, causing uneven heat transfer rates within the exchanger.

Although the entropy generation values were relatively small (for parallel flow, Sgen =0.00129kJ/K), the presence of entropy generation indicates that the process is not internally reversible. Temperature gradients within the exchanger and finite temperature differences during heat transfer introduce internal irreversibilities, which contribute to entropy generation.
</p>