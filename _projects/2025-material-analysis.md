---
layout: project
title: Mechanics of Material Analysis on Torque Wrench
description: This project pulls together topics such as materials selection, fracture, fatigue, strain gauges, stress analysis and finite analysis.
technologies: [ANSYS, Fusion 360,  MATLAB]
image: /assets/images/material.png
---

For our MAE 3270 Mechanics of Material design project, we created an instrumented 3/8"-drive torque wrench rated for 600 in-lbf. The goal was to design a lightweight handle that could survive static, fracture, and fatigue loading while producing a clear strain-gauge signal at the rated torque. Starting from a simple rectangular steel baseline, I used MATLAB hand calculations and ANSYS finite-element analysis to iterate the geometry, reduce stress concentrations near the head, and tune the gauge location. I selected 7075-T6 aluminum for its high strength-to-weight ratio and modeled the final shape in Fusion 360 before importing it into ANSYS for detailed stress and strain contour plots. The final design meets the course safety factor requirements and achieves a sensitivity of about 1.3 mV/V at 600 in-lbf, providing a more responsive and efficient torque wrench for measurement applications.

[View Full paper]({{ "/assets/material.pdf" | relative_url }}) in PDF.