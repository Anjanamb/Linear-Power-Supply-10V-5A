# Linear Power Supply — 10 V, 5 A

>A linear bench power supply design targeting 10 V output at up to 5 A. This repository includes concept, simulations, PCB layout, enclosure model, presentation slides, and a project report.

Warning: This project involves mains voltages. Only qualified individuals should build or test it. Follow proper electrical safety practices and applicable standards.

---

## Features and topology

- Step‑down transformer from 230 V AC to low‑voltage AC
- Linear regulation to 10 V DC (target), up to 5 A load
- Protection and control blocks:
  - Short‑circuit protection (fast electronic fuse behavior)
  - Over‑voltage protection (crowbar/thyristor-based)
  - Negative‑voltage protection at output
  - Foldback current limiting
  - Fan regulation for thermal management
- PCB layout (Altium), 3D enclosure (SolidWorks), and circuit simulations

---

## Repository structure

```
Linear-Power-Supply-10V-5A
├─ Circuit/
│  ├─ Fan-Regulation_Circuit.png
│  ├─ Fan-Regulation_Simulation.ms14
│  ├─ Main_Regulation_Circuit.png
│  ├─ Over-Voltage_Protection.png
│  ├─ Short-Circuit_Protection.png
│  └─ Simulation Circuit.ms14
├─ Datasheets/Over Voltage           # Related component datasheets
├─ PCB                               # Altium Designer PCBs
├─ Enclosure_Design.SLDASM           # SolidWorks assembly
├─ Presentation.pptx
├─ Project Report.pdf
├─ components & datasheets.ptpm      # project components/datasheets pack (tool-specific)
└─ README.md
```

Notes
- `.ms14` files are NI Multisim simulation projects.
- `PCB.PcbDoc` is an Altium PCB document (no schematic is included here; keep images in Circuit/ for reference).
- The SolidWorks assembly is provided for enclosure/mechanical context.

---

## Getting started

- Simulations (NI Multisim)
  1. Open the `.ms14` files in Circuit/.
  2. Run the simulations to validate foldback limiting, protections, and fan regulation behavior.

- PCB (Altium Designer)
  1. Open `PCB.PcbDoc`.
  2. Verify footprint libraries and design rules (clearances, track widths for 5 A).
  3. Perform DRC and generate fabrication outputs (Gerbers/ODB++, drill, assembly).

- Enclosure (SolidWorks)
  1. Open `Enclosure_Design.SLDASM`.
  2. Check board outline, mounting holes, airflow path for the cooling fan and heatsink.

- Documentation
  - `Project Report.pdf`: overview, block diagrams, simulation plots, and discussion.
  - `Presentation.pptx`: summary slides for quick review.

---

## Electrical and safety considerations

- Mains isolation: Use a certified transformer (e.g., 230 V AC to ~15 V AC, suitable current rating).
- Thermal: Ensure adequate heatsinking and forced airflow. Linear dissipation can be high at low output voltages/high currents.
- Protection devices: Validate thyristor/crowbar component ratings and trip thresholds on hardware.
- Wiring and creepage/clearance: Maintain safe spacings on AC side, shroud terminals, and fuse appropriately.

---

## Verification checklist

- Simulations
  - Output regulation at 10 V across expected load range
  - Foldback limiting and short‑circuit behavior
  - Over‑voltage trip and recovery
  - Fan control thresholds

- PCB and mechanical
  - Copper widths/vias sized for 5 A with acceptable temperature rise
  - Heatsink attachment and airflow clearances
  - Connector ratings and polarity
  - Mounting holes align with enclosure

- Bring‑up
  - First power via an isolation transformer and variac/current‑limited source
  - Dummy load for staged testing (resistive load bank)
  - Scope measurements for ripple, transient response, and protection triggers

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

## Acknowledgements

Thanks to the project team and course for guidance. See Project Report.pdf for details and references.

---
