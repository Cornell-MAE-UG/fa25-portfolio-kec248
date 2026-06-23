---
layout: project
title: "No Fly Zone — SLF Trap"
description: "A spotted lanternfly lure and trap for vineyards, developed for Cornell CALS Extension, E&J Gallo Winery, and National Grape."
technologies: [3D Printing, Arduino, CAD]
image: /assets/images/fig1.jpg
imagealt: Cross-sectional diagram of the spotted lanternfly trap prototype
show_on_home: true
order: 2
---

## Table of Contents

[Project Overview](#project-overview)  
[Design Solution](#design-solution)  
[Functional Prototype](#functional-prototype)  
[Testing and Results](#testing-and-results)  
[Recommendations](#recommendations)  
[Figures and Bill of Materials](#figures-and-bill-of-materials)

---

## Project Overview

The spotted lanternfly (*Lycorma delicatula*, SLF) is an invasive species that poses a growing threat to vineyards. SLFs feed on grapevines, reduce sap flow, contaminate grapes during harvest, and contribute to crop loss. Current removal methods are difficult to scale across large vineyards because they are labor-intensive and can interfere with normal vineyard operations.

For this project, our team designed **No Fly Zone**, a trellis-mounted lure and trap intended to reduce SLF population density at the vine level without damaging grapevines. The project was developed for Cornell CALS Extension, E&J Gallo Winery, and National Grape.

<div class="figure-section">

  <div class="figure-block">
    <p>
      <strong>Spotted Lanternfly:</strong> The target invasive species for the No Fly Zone lure-and-trap system.
    </p>
    <img src="{{ '/assets/images/SLF.jpeg' | relative_url }}" alt="Spotted lanternfly" class="report-figure">
  </div>

</div>

---

## Design Solution

No Fly Zone uses a two-stage system: attraction followed by capture. A wintergreen-oil-soaked sponge placed inside the device attracts SLFs toward the housing. Once the insects enter, a motor-driven rotating disk mechanism guides them downward into an isolated, removable collection chamber.

The device is designed to hang externally from vineyard trellises, avoiding direct contact with grapes while allowing SLFs to be removed directly from the vine environment. The long-term concept includes solar power, replaceable capture chambers, and electronic monitoring for large-scale vineyard deployment.

---

## Functional Prototype

Our first functional prototype was primarily composed of 3D-printed components and an Arduino-controlled motor system. The main assembly included a weather-shielding top cap, outer housing with SLF entryways, rotor and stator disk mechanism, drive shaft, DC motor, quarantine tubes, and a screw-in collection chamber.

The electronics system used an Arduino, NPN transistor, slide switch, LED indicator, and 4xAA battery pack to control and power the rotating mechanism. A wintergreen-oil sponge was placed inside the lower housing to act as the lure.

**Total BOM cost:** $58.80

### Assembly Summary

1. Glue the two top shade pieces together.
2. Assemble the Arduino motor-control circuit.
3. Insert the stator components and spacing ring onto the drive shaft.
4. Press-fit the shaft into the rotor.
5. Attach the shaft to the motor and seat the motor in its housing.
6. Slide the motor, stator, rotor, and spacer assembly into the main housing.
7. Insert the circuitry, battery pack, and wintergreen oil sponge into the lower housing.
8. Align the quarantine tubes with the collection chamber lid.
9. Screw the collection chamber onto the bottom of the housing.
10. Attach string to the top for trellis mounting.

---

## Testing and Results

### Mechanical Rotation Test

The rotor was powered and manually rotated through a full 360° range of motion to check for interference between the 3D-printed components.

**Result:** The rotor completed a full rotation without interference. However, the taped shaft-to-motor connection displaced the assembly slightly and prevented full seating.

**Design update:** Replace the taped connection with adhesive or a more rigid mechanical connection in the next iteration.

### Minimum Motor Voltage Test

The motor was tested with the rotor attached to determine the minimum voltage required for startup and continuous rotation.

**Results:**

- Continuous rotation: **1.74 V**
- Startup voltage: **2.47 V**

The 6V battery pack provided sufficient voltage headroom for operation.

### Minimum Speed Test

The minimum sustained rotor speed was measured under battery power.

**Result:** The lowest sustained speed was **45 RPM**.

Although the mechanism was functional, 45 RPM was likely too fast for a gentle insect trap. A lower-speed motor or stepper motor would allow smoother, more controlled rotation.

### Success Criteria

| Criterion | Measurement | Result |
|---|---|---|
| Hangable on grapevine trellis | Mass ≤ 1 kg | Met |
| Compact prototype | Volume ≤ 1 L | Met |
| Simple user operation | On/off in ≤ 5 seconds | Met |
| Continuous operation | ≥ 24 hours of runtime | Met with battery testing |

The prototype met the main success criteria for size, usability, and mechanical functionality. Battery calculations also indicated that the 4xAA battery pack could power the device for approximately six days, exceeding the 24-hour runtime target.

---

## Recommendations

The prototype demonstrated that a compact, 3D-printed, motorized SLF trap is mechanically feasible. However, several improvements would be needed before large-scale vineyard deployment.

Future iterations should focus on replacing the motor with a slower, lower-power option, integrating solar panels and rechargeable batteries, reducing overall size and material usage, and improving the shaft-to-motor connection. Further testing with live SLFs in a controlled environment would also be necessary to quantify attraction and capture performance.

Another future improvement would be replacing or supplementing wintergreen oil with a 60 Hz speaker-based lure. This could reduce maintenance requirements by eliminating the need to replace oil as the scent fades. Electronic monitoring could also help growers identify which traps are full, low on power, or malfunctioning, reducing the labor required to manage traps across an entire vineyard.

Overall, No Fly Zone provides a scalable proof of concept for reducing spotted lanternfly population density while minimizing labor and avoiding physical damage to grapevines.

---

## Figures and Bill of Materials

<div class="figure-section">

  <div class="figure-block">
    <p>
      <strong>Fig 1:</strong> Cross-sectional diagram of the lure-and-trap prototype, showing the shielding, SLF entryway, Arduino-driven rotating trap disk, quarantine tubes, and removable screw-in collection chamber.
    </p>
    <img src="{{ '/assets/images/fig1.jpg' | relative_url }}" alt="Cross-sectional diagram of the SLF lure-and-trap prototype" class="report-figure">
  </div>

  <div class="figure-block">
    <p>
      <strong>Fig 2:</strong> Top-down view of the rotating gate mechanism, showing how the rotor guides SLFs into the collection tubes.
    </p>
    <img src="{{ '/assets/images/fig2.jpg' | relative_url }}" alt="Top-down view of rotating gate mechanism" class="report-figure">
  </div>

  <div class="figure-block">
    <p>
      <strong>Fig 4:</strong> Arduino wiring diagram for the motor-control system, operated by a slide switch and powered by 4xAA batteries.
    </p>
    <img src="{{ '/assets/images/fig4.jpg' | relative_url }}" alt="Arduino wiring diagram for motor-control system" class="report-figure">
  </div>

  <div class="figure-block">
    <p>
      <strong>Fig 5:</strong> Electrical schematic for the motor-control system.
    </p>
    <img src="{{ '/assets/images/fig5.jpg' | relative_url }}" alt="Electrical schematic for motor-control system" class="report-figure">
  </div>

  <div class="figure-block">
    <p>
      <strong>Bill of Materials:</strong>
    </p>
    <img src="{{ '/assets/images/BOM.jpg' | relative_url }}" alt="Bill of materials table" class="report-figure">
  </div>

</div>
