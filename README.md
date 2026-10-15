# Dual Helix Antenna Design and Simulation 📡

This repository contains the design, theoretical analysis, and simulation results of a **Dual Helix Antenna** operating in the L1 GPS frequency band (1.57542 GHz). The project focuses on achieving Right-Hand Circular Polarization (RHCP) for high-reliability links in satellite communications.

This project was developed as part of the EC343: Antenna Theory course at the Sardar Vallabhbhai National Institute of Technology (SVNIT)
---

## 🎯 Aim
To design and simulate a dual helix helical antenna using **CST Studio Suite** (CST Microwave Studio), optimizing parameters for axial mode operation to achieve circular polarization.

## 🧠 Theory

### Dual Helix Antenna
A Dual Helical Antenna consists of two parallel helical conductors wound together along a common axis. Operating in **axial mode**, it produces circularly polarized (CP) radiation along the longitudinal axis. Compared to a single helix, the bifilar (dual) structure offers:
* Wider bandwidth
* Improved impedance matching
* Better polarization purity
* Reduced cross-polarization

**Key Design Parameters:**
* **Helix radius ($R$):** Affects beamwidth and impedance.
* **Pitch angle ($\alpha$):** Controls axial mode efficiency.
* **Number of turns ($N$):** Influences gain and directivity.
* **Spacing between helices ($S$):** Affects coupling and polarization purity.

### Why Axial Mode & Circular Polarization?
Axial mode radiation inherently generates circularly polarized waves. This is critical for systems like GNSS (GPS) to mitigate:
1. **Polarization Mismatch Loss:** CP ensures a robust link regardless of the rotational alignment between the transmitting satellite and the receiving antenna.
2. **Faraday Rotation:** CP waves are immune to the twisting of the polarization plane caused by the Earth's ionosphere.

### Transmission Line (Meander Line)
A meander line is used for impedance matching and phase shifting to ensure the required $180^\circ$ phase difference between the two helices. 
* Effective dielectric constant ($\epsilon_{eff}$) calculated for FR4 substrate: **3.33**
* Guided wavelength ($\lambda_g$): **104.35 mm**

---

## 📐 Design Parameters & Calculations

Operating Frequency: **$f = 1.57542 \text{ GHz}$ (GPS L1 Band)**
Free-space Wavelength: **$\lambda_0 = 190.57 \text{ mm}$**

We simulated three primary configurations. Below is the summary of the design parameters:

| Parameter | For $\lambda$ | For $2\lambda$ | For $r = 50\text{mm}$ |
| :--- | :--- | :--- | :--- |
| **Circumference $C$ (mm)** | 190.57 | 381.15 | 314.16 |
| **Radius $R$ (mm)** | 30.34 | 60.63 | 50.00 |
| **Pitch spacing $S$ (mm)** | 40.42 | 80.85 | 84.20 |
| **Number of turns $N$** | 6 | 6 | 6 |
| **Height $H$ (mm)** | 242.52 | 485.10 | 505.21 |
| **Wire radius $r_{wire}$ (mm)**| 0.5 | 0.5 | 0.5 |
| **Pitch angle $\alpha$ (deg)** | 12 | 12 | 15 |

---

## 💻 Simulation Methodology

The design process in CST Studio Suite involved:
1. Defining the ground plane and FR4 dielectric substrate.
2. Generating the helical coil using the CST Macro tool.
3. Mirroring the spiral by $180^\circ$ in the Z-plane to create the dual (bifilar) structure.
4. Designing the meander line transmission network for impedance matching.
5. Defining discrete excitation ports and simulating for S-parameters and Farfield directivity.

---

## 📊 Results and Parametric Studies

Various configurations were simulated, including single helix, dual helix without transmission lines, and dual helix with transmission lines. Parametric studies were conducted by varying the antenna height and ground plane radius.

### Key Finding (Optimized Final Configuration)
The project successfully demonstrated the electromagnetic behavior of the dual-helix antenna, achieving resonance near the targeted 1.575 GHz frequency with good impedance matching and stable circular polarization. 

The optimized configuration parameters are:
* **Height ($h$):** 500 mm
* **Turns ($N$):** 6
* **Pitch Angle ($\alpha$):** $15^\circ$
* **Spacing ($s$):** 40.42 mm
* **Radius ($R$):** 30.33 mm
* **Wire Radius ($r_{wire}$):** 0.5 mm
* **Ground Radius ($r_{gnd}$):** 55 mm

*(Note: S-Parameter graphs, Farfield directivity plots, and Impedance charts are documented in the detailed project report).*

---

## 🚀 Conclusion
The CST simulation validates the suitability of the dual-helix design for the GPS L1 frequency band. The use of a meander transmission line successfully provided the necessary phase shifts, and the axial mode operation delivered the required circular polarization and directivity for satellite telemetry applications.
