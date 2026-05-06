---
layout: project
title: "No Fly Zone — SLF Trap"
description: "A spotted lanternfly lure and trap for vineyards, developed for Cornell CALS Extension, E&J Gallo Winery, and National Grape."
technologies: [3D Printing, Arduino, CAD]
image: /assets/images/SLF.jpeg
imagealt: Spotted lanternfly trap prototype
show_on_home: true
---


## Table of Contents
[Client Pitch](#client-pitch)
[Functional Prototype](#functional-prototype)
[Client Report](#client-report)

## Client Pitch

### Problem Statement
The spotted lanternfly (Lycorma delicatula, SLF) is an invasive species spreading prolifically throughout North America. SLFs feed on grapevines, depleting nutrients and reducing crop yield, and they remain on vines during harvest, contaminating the grapes. Economic losses to the grape industry in the Finger Lakes AVA alone are estimated to reach $1.5 million in the first year of infestation, with damages projected to double annually. Grapevines under heavy infestation have been shown to use 38% less water due to reduced sap flow, reflecting significant physiological stress. Current management options are difficult to deploy at scale across large vineyards during the growing season.

### Why It Matters
Reducing SLF population density before harvest would improve both yield and grape quality. It would also reduce SLF repopulation across seasons, protecting the long-term viability of the vineyard. Adult SLFs are the primary threat: they consume the most plant sap and produce honeydew that promotes sooty mold growth, further reducing photosynthetic capacity and affecting grape appearance.

### Proposed Direction: "The Lure"
A device hung from a trellis uses a dual-attraction system — a wintergreen-oil-soaked sponge surrounding a 60 Hz speaker — to draw SLFs in. Once inside, a motor-driven rotating trap disk guides them down into a removable screw-in capture chamber. The device is powered by an onboard solar cell.
Minimum viable product: A plastic housing with a wintergreen oil lure and a one-way valve entrance (resembling a heart valve) that allows SLFs to enter but not exit.
Long-term product: Full dual-lure system with rotating trap disk, quarantine tubes, replaceable capture chamber, and solar power.

### Key Risks

Efficacy: SLF attraction to the lure cannot be easily tested in a classroom setting; field testing will be required.
Cost: Deploying one device per vine across a large vineyard could be prohibitively expensive.
Maintenance: Manual servicing of each trap (emptying chamber, replacing components) requires significant labor at scale.

### Questions for the Client

What financial investment would be available for full-scale deployment? (Informs how many units are feasible and what per-unit cost target we should design toward.)
How much labor is realistically available for ongoing maintenance? (Informs how often the capture chamber needs to be serviceable and whether automation of any maintenance step is worth pursuing.)

References:

Source 1 — JIPM: SLF economic impact
Source 2 — Sci. Dir.: Grapevine sap flow study
Source 3 — JEE: SLF management


## Functional Prototype

No Fly Zone's first functional prototype is a SLF lure and trap that uses wintergreen oil as an attractant and a motor-driven rotating disk mechanism to guide insects into a removable capture chamber. The prototype was 3D printed and assembled with an Arduino-controlled DC motor, slide switch, battery pack, and screw-in storage container.

### Design Overview
The trap consists of a weather-shielding top cap, an outer housing with SLF entryways, an internal rotating disk (rotor + stator) driven by a DC motor via a drive shaft, quarantine tubes that channel insects away from the motor, and a screw-in capture chamber at the base. A wintergreen-oil-soaked sponge sits in the lower housing to attract insects. An Arduino controls the motor, toggled by a slide switch; an LED indicates that the motor is running.

Total BOM cost: $58.80
Key components include: 3D-printed housing, rotor disc, stator disc, rotors, stators, quarantine tubes, and top shade (RPL-fabricated); drive shaft (McMaster #89845K71, $1.15); DC motor (1.5–5V); Arduino processor; NPN transistor; 6V battery pack; breadboard; wintergreen oil ($7.99); sponge ($2.99); slide switch; green LED; and wiring.

### Assembly Instructions

1. Glue the two top shade pieces together.
2. Assemble the circuit according to the wiring diagram (Arduino → NPN transistor → DC motor, powered by 6V battery pack, with slide switch and LED).
3. Insert the small stator pieces into the stator disc. Slide the stator and its spacing ring onto the drive shaft.
4. Press-fit the drive shaft into the rotor piece.
5. Solder the drive shaft to the motor shaft, then seat the motor in its housing.
6. Slide the motor + stator + rotor + spacer ring assembly into the main housing. Insert the circuitry, battery pack, wintergreen oil sponge, and large spacer ring into the         lower housing beneath the mechanism.
7. Fit the storage container lid into the bottom of the housing, aligning the quarantine tubes with the holes.
8. Screw the storage container onto the bottom of the housing.
9. Set the top shade into position and attach hanging string to the top.

### Design Tests
Test 1 — Degree of rotation (motion & interference)

Testing: Motor was powered on and the rotor was also spun by hand to check for part alignment and interference through a full 360° range of motion.
Result: No interference; full 360° rotation confirmed. However, the shaft-to-motor connection (taped) displaced component seating, preventing the assembly from sliding down fully.
Conclusion: Replace tape connection with adhesive glue for the next iteration to ensure proper component seating.

Test 2 — Minimum motor voltage (with rotor attached)

Testing: Rotor attached to motor; voltage swept upward to find minimum for continuous motion and for startup.
Result: Continuous motion requires 1.74 V; startup requires 2.47 V.
Conclusion: Current 6V battery setup provides sufficient headroom. Arduino PWM output will be tuned accordingly.

Test 3 — Minimum rotating speed

Testing: Minimum sustained motor speed measured with shaft and rotor attached under battery power.
Result: Minimum sustained speed is 45 RPM.
Conclusion: 45 RPM may be too fast to gently guide insects rather than fling them. A stepper motor will be evaluated for the next iteration to allow slow, controlled rotation.

### Success Criteria
No Fly Zone is designing a SLF lure that attracts insects via wintergreen oil and captures them using a rotating trap disk that guides them into a lower storage chamber, powered continuously by a motor.
#CriterionMeasurementPriority1Hangable on a grapevine trellis; mass ≤ 1 kgWeigh assembled unit on a scaleMinimize mass2Packed volume ≤ 1 LMeasure outer dimensions, calculate volumeMinimize volume3User can turn on/off with a single mechanism in ≤ 5 secondsTime 5 testers operating the switch without instructionNot a priority to improve beyond threshold4Operates continuously for ≥ 24 hours under solar powerRun unit on solar input, log runtime until failureMaximize runtime
Exhibit demo: Criterion 3 (the on/off switch) will be demonstrated live. A tester will be handed the assembled trap and asked to turn it on without instruction; success or failure is immediately observable and ties directly to the usability criterion.


## Client Report

### Context and Problem Statement

The spotted lantern fly (Lycorma delicatula), also known as SLFs, is an invasive species spreading prolifically throughout North America. The SLFs remain on grapevines during the harvesting process, contaminating the grapes and further decreasing yields. There is currently no efficient way to remove the SLF without damaging the grapevine, and that isn't labor-intensive. As a result, these insects continue to feed on vines and remain present during harvest, contributing to reduced yield. This product aims to reduce the population density of the SLFs, a vine-level removal process, without causing physical damage to the grapevines and minimizes labor requirements.

### Final Prototype and Application

Our team designed and developed a trellis-mounted device that attracts and removes spotted lanternflies directly from grapevines using a combination of sensory lures and motorized capture (fig 1). The device operates in 2 stages, first the attraction of the SLF followed by the capture. Wintergreen oil, a known SLF attractant, will be placed in the opening of the device to lure the SLF’s into the device. Once inside, the geometry of the enclosure guides them to the second chamber, where a geared DC motor drives a rotating, toothed mechanism that physically directs the SLFs into an isolated, removable collection chamber (fig 2). This motorized system ensures continuous movement to prevent escape while minimizing power requirements. The device is designed to operate continuously during the growing season. Lastly, the system is externally mounted and avoids direct contact with the grapes, meaning it removes SLFs without causing damage to the grapevines.

### Testing and Results

The first success criterion was to create a small, lightweight product, setting a target of 1 kg mass and 1 L volume. A small, lightweight product makes installation and transportation of the device easier. The second success criterion was to have a product with a single, intuitive on/off switch, to make the transition to using this product as seamless as possible. The third success criterion was being able to operate continuously for 24 hours without running out of power. Ideally, with a solar power source, this means that the product should be able to operate indefinitely on solar power. Due to time constraints, we evaluated this success criterion with battery power.

Testing the mechanical operation of the rotor, the function of the motor, and the battery demonstrated the feasibility of our design and manufacturing process. We were able to 3D print most parts and use a 4xAA battery pack to power our device, resulting in a small, lightweight, energy-efficient device.

### Prototype and Testing Details

Our prototype consisted of two main subsystems: A mechanical trapping mechanism and an electronics assembly, housed within a 3D structure. The structural housing is composed of multiple 3D printed components including a shielded canopy top, a cylindrical main body, and a removable screw in the collection chamber. Within the collection chamber is a wintergreen oil soaked sponge to lure the SLFs into the device. The trapping mechanism uses a rotating disk(rotor) and a fixed disk(stator) whose intersecting slots funnel the SLFs downwards without crushing them as the rotor spins. The rotor is driven by a DC motor connected to a drive shaft, controlled through an NPN transistor by an Arduino and operated by a side switch. An LED light indicates when the motor is active. A flyback diode protects the motor, and all components are communally grounded. The electronics and battery packs are housed within the main body beneath the trapping mechanism, and the collection chamber screws into the bottom for easy removal and emptying.

Referenced below are the steps for assembly:

#### Assembly instructions

1. Glue the 2 top shade pieces together.
2. Assemble the circuit according to the diagram.
3. Insert the small stator pieces into the stator. Slide the stator and its spacing ring onto the shaft.
4. Press fit the shaft into the rotor piece.
5. Solder the shaft into the motor’s shaft, then place the motor into its housing.
6. Slide the current assembled pieces (motor, stator, rotor, spacer ring) into the housing. Insert the circuitry, battery, and wintergreen oil sponge into the housing beneath the other pieces, along with the big spacer ring.
7. Fit the storage container lid into the bottom of the housing, making sure the tubes align with the holes.
8. Screw the storage container into the bottom of the housing.
9. Place the main component on top into position and attach string at the top to hang

As we were focused on scalability, we wanted our 3D printed components to be interchangeable and assembled with full clearance and space for other components. The first test we did was to make sure that all gate components could rotate 360 degrees as intended without friction, to evaluate the feasibility of making most parts out of 3D printed plastic. After assembling the prototype, we rotated the trap 360 degrees to confirm it spun smoothly (only slight power losses and friction), confirming our main mechanical component of our device to be operational. Because we can 3D print most components, our prototype is able to be lightweight, which is directly related to our first success criterion.

The second test was testing the minimum voltage on the motor to start and maintain rotation, which was 2.47 V and 1.74 V respectively. This was within the capability of our 6V battery pack, and meant that we could keep the battery as is. We wanted to use as lightweight and compact a battery pack as possible, which relates to our first success criterion. Additionally, the batteries we chose for longevity (4x AA), and after current calculations, can last approximately six days (fulfilling our third success criterion of lasting for 24 hours).

Lastly, we tested the minimum rotating speed, which informed us on the choice of motor. The minimum rotating speed without stopping due to friction was 45 rpm, which was too fast for a spinning fly trap, and it could scare the lanternflies away. We decided to replace the motor with a different one that was able to rotate more slowly at 20 rpm and also required less power, which makes for smoother and more controlled operation.

### Conclusion and Recommendation

Our design was built with the idea of scalability. While our prototype works effectively, adjustments would have to be made if it were to be implemented on a larger scale. A large reason why we chose an arduino instead of a simpler microcontroller was the ability to add more features in the future. To monitor battery and functionality of multiple devices across the vineyard, a control panel could be used to display and communicate with the arduinos so that the client would only need to service devices that are in need of it, instead of individually checking them.

Another solution to implement into our design could be solar panels. Since batteries must be replaced, it is inefficient to install hundreds of these prototypes across a vineyard. Having rechargeable batteries powered by solar panels allows the client to leave the traps for much longer periods.

Another factor to consider is the oil we use. While using wintergreen oil is effective for smaller scale projects, having to replace the oil every few days so the scent does not fade is an additional labour cost. If we instead had a speaker powered by the solar panels emitting a 60 Hertz frequency (a frequency that has been shown to attract SLFs), we could replace the need for wintergreen oil entirely.

We could also potentially reduce the size to make it more cost effective and lighter, making the device more practical for large-scale deployment. Specifically, we could test a different design shape rather than a cylinder with a hood. Another solution could be to move the motor to a different section of the design, allowing for space optimization in the body of the design. By refining the geometry and minimizing unnecessary material, the system could become more compact and easier to install across vineyard trellises. Reducing weight would also decrease structural strain and simplify mounting, while lowering material usage would directly reduce production costs.

Given our resources and the scope of the class, most of the functional testing has already been completed. Our device met all our success criteria, operating efficiently and allowing model SLFs to be captured. To have a stronger pitch, tests in a controlled environment with actual SLFs should be conducted to quantify attraction to our device.


---

## Figures and Bill of Materials

<div class="figure-section">

  <div class="figure-block">
    <p>
      <strong>Fig 1:</strong> Cross-sectional diagram of the lure-and-trap prototype, showing key components including the shielding, SLF entryway, Arduino-driven rotating trap disk, quarantine tubes that keep bugs away from the motor, and the removable screw-in collection chamber.
    </p>
    <img src="{{ '/assets/images/fig1.jpg' | relative_url }}" alt="Cross-sectional diagram of the SLF lure-and-trap prototype" class="report-figure">
  </div>

  <div class="figure-block">
    <p>
      <strong>Fig 2:</strong> Top-down view of the rotating gate mechanism, showing the direction of rotation that forces spotted lanternflies down into the collection tubes.
    </p>
    <img src="{{ '/assets/images/fig2.jpg' | relative_url }}" alt="Top-down view of rotating gate mechanism" class="report-figure">
  </div>

  <div class="figure-block">
    <p>
      <strong>Fig 4 & 5:</strong> Electrical schematic and Arduino writing diagram for the motor control system, controlled by a slide switch and powered by 4x AA batteries
    </p>
    <img src="{{ '/assets/images/fig4.jpg' | relative_url }}" alt="Arduino wiring diagram for motor control system" class="report-figure">
    <img src="{{ '/assets/images/fig5.jpg' | relative_url }}" alt="Electrical schematic for motor control system" class="report-figure">
  </div>

  <div class="figure-block">
    <p>
      <strong>Bill of Materials:</strong>
    </p>
    </p>
    <img src="{{ '/assets/images/BOM.jpg' | relative_url }}" alt="Bill of materials table" class="report-figure">
  </div>

</div>
