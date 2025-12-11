---
layout: project
title: High-Speed Drone – Full CAD & Aerodynamic Analysis
description: A custom-designed high-speed drone frame built in Autodesk Fusion 360, focused on aerodynamics, pressure edurance, and real-world flight applications.
technologies: [Audodesk Fusion 360, stream flow simulation]
image: /assets/images/extr.png
---

EXTR V1 is a conceptual high-speed racing drone that I fully designed in CAD, including the central fuselage, wing-like arms, and motor housings. I used CFD simulations to study airflow and friction over the body and propeller pods, then iterated the geometry to smooth flow separation and lower drag. This project showcases my skills in 3D modeling, design for aerodynamics, and simulation-driven refinement.

<!-- Pressure / friction result -->
<div>
  <img
    src="{{ '/assets/images/extr-pressure.png' | relative_url }}"
    alt="CFD pressure and surface friction visualization"
    class="inline-image-l"
  >
  <p><strong>Pressure & Surface Friction (AirShaper).</strong> This AirShaper simulation shows how pressure and surface friction are distributed over the drone. High-pressure zones around the nose, nacelles, and leading edges highlight where the flow loads the structure most, guiding the rounded nose and smoother arm transitions I used to reduce drag and peak stresses.</p>
</div>
<div style="clear: both;"></div>

<!-- Streamlines / velocity result -->
<div>
  <img
    src="{{ '/assets/images/extr-flow.png' | relative_url }}"
    alt="CFD streamline and velocity visualization"
    class="inline-image-l"
  >
  <p><strong>Streamlines & Velocity Field (AirShaper).</strong> This AirShaper streamline plot visualizes how the flow moves around the drone. The smooth, parallel streamlines over the body and the reduced wake behind the fuselage indicate attached flow and lower separation, confirming that the refined pod and fuselage geometry improves aerodynamic efficiency.</p>
</div>
<div style="clear: both;"></div>


