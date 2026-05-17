---
layout: project
title: High Speed Drone - EXTR V2 (In progress...)
description: A custom-designed high-speed drone chassis built in Autodesk Fusion 360, focused on aerodynamics, pressure endurance, and real-world flight applications.
technologies: [Autodesk Fusion 360, SimScale]
image: /assets/images/extr2.jpg
---

<div class="project-hero">
  <img src="{{ '/assets/images/extr2.jpg' | relative_url }}" alt="EXTR V2 High Speed Drone Hero Render" style="width: 100%; border-radius: 8px; margin-bottom: 1rem;">
  <p style="font-size: 1.2rem; font-weight: 500; color: #555;">
    Designing a custom aerodynamic chassis optimized for extreme high-speed FPV flight, targeting minimal drag and optimal thermal management for internal components.
  </p>
</div>

<hr>

## Project Overview

### Objective
To design and manufacture a custom drone frame capable of sustaining high speeds while protecting critical internal electronics—like the VTX and ESCs—from extreme aerodynamic pressure and thermal throttling.

### Aerodynamic Approach
Moving away from traditional open-frame quadcopters, the EXTR V2 utilizes a teardrop fuselage to maintain attached airflow. Initial CFD analysis using SimScale validated a significant reduction in frontal drag and identified key pressure zones around the motor shrouds.

### Next Steps
Transitioning from CAD validation to physical prototyping. Upcoming phases include 3D printing the chassis utilizing high-strength, temperature-resistant materials like Carbon Fiber Nylon (PA-CF) and conducting real-world flight testing to validate the simulated aerodynamic gains.

---

## Aerodynamic Simulation & CAD

<div class="image-grid" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin-top: 20px;">

  <figure style="margin: 0;">
    <img src="{{ '/assets/images/extr67.png' | relative_url }}" alt="Fusion 360 CAD Model" style="width: 100%; border-radius: 4px;">
    <figcaption style="font-size: 0.9rem; color: #666; margin-top: 8px; text-align: center;">
      Complete mechanical assembly modeled in Fusion 360, featuring aerodynamic motor shrouds.
    </figcaption>
  </figure>

  <figure style="margin: 0;">
    <img src="{{ '/assets/images/extr22.png' | relative_url }}" alt="Velocity Streamline Analysis" style="width: 100%; border-radius: 4px;">
    <figcaption style="font-size: 0.9rem; color: #666; margin-top: 8px; text-align: center;">
      SimScale velocity streamline analysis demonstrating attached flow over the main fuselage.
    </figcaption>
  </figure>

  <figure style="margin: 0;">
    <img src="{{ '/assets/images/extr23.jpg' | relative_url }}" alt="Pressure Contour Mapping" style="width: 100%; border-radius: 4px;">
    <figcaption style="font-size: 0.9rem; color: #666; margin-top: 8px; text-align: center;">
      Pressure contour mapping used to identify high-drag zones on the chassis.
    </figcaption>
  </figure>

  <figure style="margin: 0;">
    <img src="{{ '/assets/images/extr24.jpg' | relative_url }}" alt="Wake Separation Analysis" style="width: 100%; border-radius: 4px;">
    <figcaption style="font-size: 0.9rem; color: #666; margin-top: 8px; text-align: center;">
      Evaluating wake separation and turbulence behind the motor mounts.
    </figcaption>
  </figure>

  <figure style="margin: 0;">
    <img src="{{ '/assets/images/extr25.jpg' | relative_url }}" alt="CFD Top Profile" style="width: 100%; border-radius: 4px;">
    <figcaption style="font-size: 0.9rem; color: #666; margin-top: 8px; text-align: center;">
      Top-down profile verifying flow symmetry across the quad arms.
    </figcaption>
  </figure>

</div>