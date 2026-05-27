# Linear Power Supply — 10 V, 5 A

> Linear bench power supply targeting **10 V / 5 A**. Concept, simulations, PCB layout, enclosure model, slides, and project report.

[![Altium](https://img.shields.io/badge/Altium-Designer-A5915F?style=flat-square&logo=altiumdesigner&logoColor=white)](https://www.altium.com/)
[![SolidWorks](https://img.shields.io/badge/SolidWorks-CAD-FF0000?style=flat-square)](https://www.solidworks.com/)
[![Multisim](https://img.shields.io/badge/Multisim-simulation-005CA9?style=flat-square)](https://www.ni.com/en/shop/electronic-test-instrumentation/application-software-for-electronic-test-and-instrumentation-category/what-is-multisim.html)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

> ⚠ **Mains voltages involved.** Only qualified individuals should build or test this. Follow proper electrical safety practices.

---

## Topology

- Step-down transformer 230 V AC → low-voltage AC
- Linear regulation to 10 V DC at up to 5 A
- Short-circuit protection (fast electronic fuse behaviour)
- Over-voltage protection (crowbar / thyristor)
- Negative-voltage protection at output
- Foldback current limiting
- Thermal management via fan-regulation circuit
- PCB layout (Altium) + 3D enclosure (SolidWorks) + Multisim simulations

## Repository structure

```
Linear-Power-Supply-10V-5A/
├─ Circuit/
│  ├─ Fan-Regulation_Circuit.png
│  ├─ Fan-Regulation_Simulation.ms14
│  ├─ Main_Regulation_Circuit.png
│  ├─ Over-Voltage_Protection.png
│  ├─ Short-Circuit_Protection.png
│  └─ Simulation Circuit.ms14
├─ Datasheets/Over Voltage/             # Component datasheets
├─ PCB/                                 # Altium PCBs
├─ Enclosure_Design.SLDASM              # SolidWorks assembly
├─ Presentation.pptx
├─ Project Report.pdf
└─ components & datasheets.ptpm
```

## License

[MIT](LICENSE) — see [anjanamb.github.io](https://anjanamb.github.io/) for more projects.
