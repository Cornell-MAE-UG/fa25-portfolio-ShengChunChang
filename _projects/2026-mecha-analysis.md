---
layout: project
title: Autonomous Cube-Collecting Robot for Mechatronics
description: This project involved the mechanical design, embedded system programming, and sensor calibration of an autonomous robot for a competitive cube-collecting match.
technologies: [Arduino, C++, 3D Printing, CAD, Embedded Systems]
image: /assets/images/mecha.png
---

For our MAE 3780 Mechatronics project, we designed and built an autonomous robot for the "Cube Craze" competition, where the objective was to collect as many 1-inch wooden cubes scattered along a midline in a 60-second span. We started with a standard "Boe-Bot" chassis and focused our mechanical design on maximizing our sweep width. Using CAD, we designed a custom U-shaped block guard, which we 3D printed with a 7% infill to keep the assembly lightweight, rigid, and cost-effective. To prevent cubes from escaping during aggressive lateral sweeps, we integrated a servo-driven pipe cleaner brush mechanism to actively sweep cubes inward. 

The robot's electrical system was controlled by an Arduino Uno, utilizing two L9110H H-bridge ICs driven via direct PORTB register manipulation for fast, simultaneous motor switching. A critical challenge was calibrating our downward-facing TCS3200 color sensor to reliably detect the field's yellow/blue midline and black perimeter. By transitioning from raw `pulseIn()` measurements to a fixed 50ms pulse-counting window, we achieved the stable readings necessary for our midline sweeping logic. After debugging erratic logic issues caused by a depleted 9V battery, our direct midline interception strategy proved highly reliable, allowing our robot to achieve a 5-1-1 competition record and peak at 7 cubes collected in a single match.

[View Original Document]({{ "/assets/mecha.pdf" | relative_url }}) in PDF.

---

## Full Project Report

### 1. Robot Design and Strategy Overview
We designed our robot specifically for the Cube Craze competition. In this event, two opposing robots have exactly one minute to collect 1-inch wooden blocks distributed along the center line. The game field features 20 blocks scattered across the center, divided into yellow and blue sides with a black boundary marking the outer edges. The structural design prioritized three main objectives: maximizing our sweeping width, ensuring reliable midline detection, and keeping the robot in constant motion for the full duration of the match. On the mechanical side, we utilized a standard Boe-Bot chassis, driving it with two wheels and stabilizing it with a rear ball caster. 

The major structural addition is a custom U-shaped, 3D-printed block guard. This component significantly expands our reach for collecting and storing blocks. We also integrated a servo-driven mechanism that spins a pipe cleaner attached to a metal rod. The spinning bristles actively pull blocks inward, preventing them from bouncing away. Both the guard and the active brush were crucial for holding onto blocks during fast lateral movements across the field.

Our electrical setup relied on an Arduino Uno. We controlled the two DC motors using L9110H H-bridge ICs, executing rapid and simultaneous switching by directly manipulating the PORTB registers on digital pins 8 through 11. To ensure quick reaction times, we mounted a TCS3200 color sensor on the underside of the chassis, orienting it forward to read the floor color early. 

Our software utilized a two-phase state machine. During the initial phase, the robot drives straight forward until the color sensor detects a transition (either yellow to blue, or blue to yellow) indicating the midline. Once the line is crossed, it stops and executes a 90-degree turn (timed at 450ms) to align itself. In the second phase, the robot sweeps laterally along the line, gathering blocks. When the sensor registers the black perimeter border, the robot backs up for 400ms, turns 180 degrees (timed at 900ms), and resumes sweeping in the opposite direction. This back-and-forth pattern continues until time expires. Our empirically calibrated color thresholds were: Black < 400, Yellow 400–660, and Blue > 660. 

### 2. Design Process Reflection
Our final design evolved significantly through multiple rounds of prototyping, especially regarding the code and the physical block-storing plow. Early brainstorming centered on the retention mechanisms. After finalizing the guard dimensions, we focused heavily on software integration and electrical wiring. 

We explored various manufacturing options for the guard but ultimately chose 3D printing. It allowed for full customization to meet competition rules while keeping the part lightweight and durable. To keep costs low and minimize weight, we printed the components with a 7% infill. This provided enough rigidity to push the blocks without exceeding our mass limits. 

The most demanding technical challenge was calibrating the color sensor. Initially, we used the standard pulse-in function to read the sensor's output period. However, this proved unreliable: yellow surfaces returned pulses that were too brief, while black surfaces caused timeout errors. We solved this by implementing a fixed 50-millisecond timing window to count rising edges, which produced stable and distinct readings. 

Another major hurdle was erratic sensor behavior when the robot ran independently on battery power, as opposed to being plugged into a computer. After systematic hardware debugging, we traced the issue to a depleted 9-volt battery supplying only 6.6 volts to the Arduino. Replacing the battery immediately restored full brightness to the sensor LED and fixed the logical errors. 

Our strategy also adapted over time. Initially, we programmed a U-shaped sweeping path, but our robot lacked the speed to execute it before opponents cleared the board. We pivoted to a direct-intercept strategy: driving straight to the midline to grab a large initial proportion of the blocks, then sweeping to retain them.

### 3. Competition Analysis
Our robot performed very well on competition day, securing 5 wins, 1 tie, and 1 loss out of 7 rounds. Given the earlier sensor issues, we were incredibly proud of this outcome. The direct midline interception strategy proved highly dependable. Interestingly, our robot possessed superior pushing power compared to many opponents, likely because our standard motors provided higher torque than modified, high-speed alternatives. 

Our biggest advantage was our wide sweep coverage. The U-shaped plow spanned roughly twice the width of the chassis, and the active brush kept blocks secured. We averaged 5 blocks per match, peaking at 7. Our single loss occurred against a much faster robot that beat us to the centerline and pushed the blocks to the edge. The tie happened in the first round when our plow became entangled with the opponent's bot. 

One area for future improvement is block retention during the 180-degree turnaround sequence. The reversal motion tended to scatter collected blocks toward the front edge of the plow. We also lost several blocks due to height discrepancies on the competition platform. A fully enclosed storage compartment would be a significant upgrade over the open plow design.

### 4. Conclusions
This project underscored the necessity of systematic hardware debugging and reliable embedded sensor calibration. Switching from raw period measurements to a fixed pulse-counting window was the breakthrough that made our color sensing viable. Furthermore, tracing complex logical failures back to a simple low-voltage battery issue was a valuable lesson in power management. 

Our iterative mechanical design resulted in a highly effective, budget-friendly sweeping plow. Combined with the active brush and our straightforward approach to the midline, the system was highly competitive. While we lacked top-end speed, our torque and wide capture area made up for it. For future iterations, optimizing the drivetrain for higher RPMs and fully enclosing the capture area would yield even better results.