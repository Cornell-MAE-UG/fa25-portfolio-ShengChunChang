---
layout: project
title: Planetary Gearbox CAD Design (Single-Stage, 3-Planet)
description: Designed and animated a single-stage planetary gearbox in Fusion 360, validated the 3.27:1 reduction with tooth-count constraints, and documented the assembly with motion studies and a BOM-style breakdown.
technologies: [Autodesk Fusion 360, Gear Train Kinematics, Rendering]
image: /assets/images/gearbox.png
---

<section>
  <h3>Overview</h3>
  <p>
  A planetary gearbox is a compact transmission that uses a sun gear, multiple planet gears, and an internal ring gear to achieve high torque density and a coaxial input/output shaft. It is widely used in robotics, automotive drivetrains, and aerospace actuators because it delivers large speed reduction in a small, lightweight package.
</p>

  <p>
    In this project, I designed and modeled a single-stage planetary gearbox in Autodesk Fusion 360 to demonstrate compact torque multiplication,
    coaxial power flow, and real mechanical packaging. The assembly includes a 33-tooth sun gear, three 21-tooth planet gears,
    and a 75-tooth internal ring gear constrained by a housing. I created motion animations to verify the kinematics and produced
    portfolio-ready visuals that show both the working mechanism and the assembly structure.
  </p>
</section>
<section>
  <h3>Animation</h3>

  <div class="media-grid">
    <!-- Video 1 -->
    <figure class="media">
      <video
        class="media-video"
        autoplay
        loop
        muted
        playsinline
        controls
        preload="metadata"
        poster="{{ '/assets/images/gearbox.png' | relative_url }}"
      >
        <source src="{{ '/assets/images/gearbox.mp4' | relative_url }}" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </figure>

    <!-- Video 2 -->
    <figure class="media">
      <video
        class="media-video"
        autoplay
        loop
        muted
        playsinline
        controls
        preload="metadata"
        poster="{{ '/assets/images/gearbox.png' | relative_url }}"
      >
        <source src="{{ '/assets/images/gearbox1.mp4' | relative_url }}" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </figure>
  </div>
</section>

<style>
  .media-grid{
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1.25rem;
    align-items: start;
  }

  .media{
    margin: 0;
  }

  .media-video{
    width: 100%;
    max-width: 520px;   /* tweak this number to make each video smaller/larger */
    height: auto;
    display: block;
    border-radius: 12px;
  }

  .media figcaption{
    margin-top: 0.5rem;
  }

  /* Stack on small screens */
  @media (max-width: 900px){
    .media-grid{
      grid-template-columns: 1fr;
    }
    .media-video{
      max-width: 100%;
    }
  }
</style>




<section>
  <h3>Design Goals</h3>
  <ul>
    <li>Create a functional planetary gear set with correct tooth-count relationships and center distances.</li>
    <li>Validate the expected reduction ratio through calculation and motion verification in Fusion.</li>
    <li>Build a clean assembly with carrier, pins, output shaft, and housing elements (manufacturable geometry).</li>
    <li>Produce motion and exploded-view animations suitable for portfolio presentation.</li>
  </ul>
</section>

<section>
  <h3>Gear Set Specification</h3>
  <ul>
    <li><strong>Sun gear:</strong> 33 teeth (input)</li>
    <li><strong>Planet gears:</strong> 21 teeth × 3</li>
    <li><strong>Ring gear:</strong> 75 teeth (internal, fixed to housing)</li>
    <li><strong>Output:</strong> Carrier + output shaft</li>
  </ul>
</section>

<section>
  <h3>Key Calculations</h3>
  <p><strong>Tooth-count constraint (planetary geometry):</strong></p>
  <p style="font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, 'Liberation Mono', 'Courier New', monospace;">
    N<sub>r</sub> = N<sub>s</sub> + 2N<sub>p</sub><br>
    75 = 33 + 2(21) &nbsp;✓
  </p>

  <p><strong>Reduction (ring fixed, sun input, carrier output):</strong></p>
  <p style="font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, 'Liberation Mono', 'Courier New', monospace;">
    i = 1 + N<sub>r</sub>/N<sub>s</sub> = 1 + 75/33 = 3.2727 : 1
  </p>

  <p><strong>Carrier speed relative to sun:</strong></p>
  <p style="font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, 'Liberation Mono', 'Courier New', monospace;">
    ω<sub>c</sub> = ω<sub>s</sub> · N<sub>s</sub>/(N<sub>s</sub>+N<sub>r</sub>) = ω<sub>s</sub> · 33/108 = 0.3056 ω<sub>s</sub>
  </p>
</section>

<section>
  <h3>CAD Workflow</h3>
  <ul>
    <li>Generated spur gears using consistent gear parameters (module and pressure angle) to ensure correct meshing.</li>
    <li>Built a component-based assembly with revolute joints for sun, carrier, and planet pins.</li>
    <li>Used motion links to enforce correct relative rotation and produce smooth, repeatable animations.</li>
    <li>Applied realistic appearances (steel/aluminum) and created render angles for a product-like presentation.</li>
  </ul>
</section>

<section>
  <h3>Deliverables</h3>
  <ul>
    <li><strong>Motion animation:</strong> Sun-driven input with visible carrier output reduction (~3.27:1).</li>
    <li><strong>Exploded/assembly animation:</strong> Communicates structure, part relationships, and manufacturability.</li>
    <li><strong>BOM-style documentation:</strong> Component naming and quantity structure for professional reporting.</li>
  </ul>
</section>

<section>
  <h3>BOM (Summary)</h3>
  <ul>
    <li>Ring Gear, 75T (fixed) × 1</li>
    <li>Sun Gear, 33T (input) × 1</li>
    <li>Planet Gear, 21T × 3</li>
    <li>Carrier Plate / Carrier Assembly × 1</li>
    <li>Planet Pins / Posts × 3</li>
    <li>Output Shaft × 1</li>
    <li>Housing / Outer Shell × 1</li>
  </ul>
</section>

<section>
  <h3>Next Improvements</h3>
  <ul>
    <li>Add bearings or bushings on planet pins and the carrier output to reflect real support and reduce friction.</li>
    <li>Add fasteners and a cover plate to fully communicate assembly method and serviceability.</li>
    <li>Create a 2D drawing package (critical dimensions + tolerances) for carrier and housing components.</li>
    <li>Run a basic stress check on pins and tooth contact under an assumed torque load.</li>
  </ul>
</section>
