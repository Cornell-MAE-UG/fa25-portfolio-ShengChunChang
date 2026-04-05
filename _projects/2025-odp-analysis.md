---
layout: project
title: Open Design Project
description: This is a collaborative school project for MAE 2250
technologies: [Fusion 360]
image: /assets/images/odp.jpg
---

## Table of Contents
* [Client Pitch](#client-pitch)
* [Functional Prototype](#functional-prototype)

---

## Client Pitch

**MAE 2250**

**Team Name:** Lanternfly Killers  
**Client(s):** Cornell CALS Extension / E&J Gallo Winery / National Grape

### Problem Statement
Just 1-2 adult spotted lantern flies (SLF) can taint a kilogram of grade slurry; with how prevalent they are, this can add up rapidly. Farmers are searching for ways of managing the SLF population without diminishing the potential crop yield. One way that the SLF population enters the crop yield is via the harvester during harvest. Finding a way to remove the flies off of the vines as the harvester intakes the grapes is important to prevent them from tainting the crop.

### Why it matters to the end user
If we reduce the amount of SLF present in the crop yield, we will be able to help the farmers financially, since less crop will be thrown away due to SLF contamination. In addition, there will be less scarcity of grape products, since more products will make their way to the shelves, allowing businesses to not lose customers or profit. The consumers will also benefit from the lower costs associated with the abundance of grape products.

### Proposed Directions
**Concept A: Blower** A system of devices attached to the front of the harvester to blow the SLF off of the vines before they can enter the harvester. This could be similar to the end of a car wash, but less strong. Attached in front of the harvester pointing outward toward the grape vines. A fan would blow a steady stream of air toward the vines, causing the SLF to fly outwards to avoid the irritation. The flow of air would also stop the SLF from flying into the harvester after they left the vine. This is better than the “status quo” of using chemicals to deter or remove SLF from the grapes, since the chemicals may end up contaminating the grape product, making it unusable. This is better than the “status quo” in the way that it doesn’t just scare away bugs but physically moves them to a singular destination and traps them.

**Concept B: Vibration Attraction Device** A set of towers vibrating at 60 Hz placed around the field to attract the SLF to liquid chemical traps. Towers with mechanical vibration devices to attract the SLF. An electrified outer cage to shock the SLF when they touch the trap. A container below to catch the dead SLF for easy removal. This is better than the “status quo” because it eliminates SLF year-round without having to continuously spray. This is better than the “status quo” because it does not require any changes to the harvester and saves money because it is a one-time purchase, not a yearly cost.

### Key risks / unknowns
* **Damage to grapes/vines:** Test by seeing how much wind store-bought grapes can take before falling off the vine. 
* **Lanternflies getting stuck in the blower:** Test with different geometries of the mechanical design of the tube. 
* **Blower’s force is not strong enough to detach lanternflies from grapes:** Take weight samples of lanternflies and their grab force to calculate the amount of wind force needed to remove them.

### Our questions
1. **When dealing with the SLFs, do they often stay on the vine when removing grapes?** *Decisions Affected:* This would change our blower design, as we would need to prototype to make sure that we do not remove grapes as well as the SLFs.
2. **If SLF contamination occurs in grape products, do the machines in the processing facilities need to be shut down and cleaned afterwards?** *Decisions Affected:* While this would not directly affect our decision making, this would clarify the impact on the end user, since we would be more aware of the negative impacts of SLF contamination, particularly in the cost of and time lost to temporarily shutting down facilities.
3. **Is there space in the fields to place a structure such as a tower?** *Decisions Affected:* If we are not able to place something in the field, we may not be able to implement our vibration solution in the currently intended method.

---

## Functional Prototype

### Purpose of the Prototype
Our plan is to design and assemble a blower mechanism that will be attached to the front of the grape harvester. This device is meant to cause the Spotted Lanternflies (SLF) to be blown off of the grape vine before the grapes enter the harvester. Because SLFs are very flighty insects, a strong enough fan may motivate them to vacate the row being harvested.

### What Was Tested
We tested multiple aspects of our initial blower design:
* **Wind pressure and speed:** We powered the motor with 5V through an Arduino Uno Minima Rev4. Because we lacked an anemometer, we calculated RPM by marking a fan blade, recording a slow-motion video, and counting the revolutions.
* **Funnel shape:** We simulated the shape of the end of the funnel using Fusion 360 software.
* **Material analysis:** We conducted a manual flex test by hand to assess the life cycle of the PLA blower.
* **Required force and pattern:** We ran a real-life simulation using tape and string as "grapes" and a cardboard lanternfly taped to a "vine". We blew air through the tube to test effectiveness.

### Outcome
* **Wind Speed:** The motor successfully generated roughly 3,500 RPM.
* **Funnel Shape:** The simulation showed that a circular funnel results in an even distribution of pressure.
* **Material:** The 3D-printed PLA funnel was slightly bendable by hand, which is acceptable for this prototype but will need to be changed for a future prototype or final product.
* **Force/Pattern:** We discovered that a sudden burst of air is more effective at displacing the "flighty" SLFs than a constant stream.
* **Future Improvements:** To improve wind pressure and speed, we plan to add a planetary gearbox to step up the motor speed. We also need to add holes to the motor housing and open the back to increase airflow, expand hole tolerances, add tube fittings to prevent air leaks, and optimize the fan blade design.