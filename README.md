Overview

This repository contains the KiCad design files, documentation, and resources for the power subsystem of a Micromouse robot developed as part of the EEE3088F course at the University of Cape Town. The Micromouse competition challenges small autonomous vehicles to navigate and solve a maze faster than any human operator, driving innovation in embedded control, power management, and sensor integration.

Key Features

Bidirectional Motor Control: Four DC motors controlled via DRV8833PWPR H‑bridges—two primary motors (200 mA each) and two auxiliary motors (500 mA each) using available power pins.

Battery Monitoring: INA219 current and voltage sensor on the I²C bus, configured with the correct pull-up address (only one of A0/A1 to ground).

Battery Charging: XL1509 buck converter from 9 V input with two charge modes (200 mA and ~600 mA ±100 mA) for a single-cell LiPo battery.

USB-C Power Delivery: HUSB237 controller to negotiate and output 9 V from a USB-C host.

External Load Switching: Two high‑side switches capable of 1 A each, driven from the 5 V rail.

Regulated Outputs: Onboard 3.3 V regulator (300 mA, 5% accuracy) and 5 V rail (1.5 A, 5% accuracy) for logic and peripheral power.

Power Control: Low‑leakage ON/OFF switch achieving <30 µA in OFF state and up to 2 A peak in ON state, able to disconnect both 5 V and 3.3 V rails.

Protection and Debug: Test points for key rails, onboard fuses, optional current‑sense resistors, and a spare INA219 footprint for rapid troubleshooting and failure recovery.## Repository Structure
