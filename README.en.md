<p align="center">
  <img src="https://raw.githubusercontent.com/ProyectoSoberana/soberana/main/logo.svg" width="350" alt="Proyecto Soberana">
</p>

# Proyecto Soberana

**Technological sovereignty from silicon to the operating system.**

Proyecto Soberana is a long-term initiative aimed at building a completely independent technology stack: from processor and motherboard design to the operating system running on top of them. The ultimate goal is to depend on no external vendor at any layer of the hardware or software stack.

---

## Motivation

Technological dependence is a form of geopolitical dependence. Every imported CPU, every proprietary operating system, and every opaque firmware layer represents a vector of external control. Proyecto Soberana seeks to reverse this by building, layer by layer, a fully audited, reproducible, open hardware and software alternative.

---

## Roadmap

| Stage | Description | Status |
|-------|-------------|--------|
| 1 | Submit Basilisk design to IHP for processor fabrication in 130nm BiCMOS | 📋 Planned |
| 2 | Fabricate motherboard (Basilisk Tester Board Rev C) and HyperRAM module (Rev A) — JLCPCB / PCBWay | 📋 Planned |
| 3 | Assemble: solder Basilisk chip to motherboard and connect HyperRAM module — validate functionality | 📋 Planned |
| 4 | Install Linux on the sovereign hardware | 📋 Planned |
| 5 | Develop motherboard and HyperRAM module with an Argentine national company | 📋 Planned |
| 6 | Acquire own 130nm lithography system (KrF — IHP BiCMOS PDK) | 📋 Planned |
| 7 | Produce sovereign chips with own lithography | 📋 Planned |

---

## Philosophy

- **Open by design:** all work is open-source and reproducible.
- **Incremental:** each stage is functional on its own and the foundation for the next.
- **Documented:** every technical decision is recorded so anyone can replicate the process.
- **Independent:** no proprietary license dependencies where avoidable.

---

## Technology Stack Architecture

```
┌─────────────────────────────────┐
│        Operating System         │  ← FreeBSD / Linux RISC-V
├─────────────────────────────────┤
│   Firmware (OpenSBI + U-Boot)   │  ← Boot stack
├─────────────────────────────────┤
│   Basilisk SoC (CVA6 RV64)      │  ← Chip fabricated at IHP 130nm
├─────────────────────────────────┤
│         Motherboard             │  ← Basilisk Tester Board (KiCad)
├─────────────────────────────────┤
│       HyperRAM Module           │  ← Daughter board Rev A
└─────────────────────────────────┘
```

---

## References

### Processor — Basilisk SoC

| Resource | Link |
|----------|------|
| Basilisk project page (ETH Zürich) | https://iis-people.ee.ethz.ch/~phsauter/basilisk/ |
| RTL design + IHP 130nm flow (upstream) | https://github.com/pulp-platform/cheshire-ihp130-o |
| RTL design + IHP 130nm flow (Soberana fork) | https://github.com/ProyectoSoberana/cheshire-ihp130-o |
| GDS ready to submit to IHP (flow output, no recompilation needed) | https://iis-people.ee.ethz.ch/~tbenz/gds/basilisk_release.gds.gz |
| Cheshire base platform | https://github.com/pulp-platform/cheshire |
| IHP Open Source PDK | https://github.com/IHP-GmbH/IHP-Open-PDK |

### Motherboard and HyperRAM module — KiCad

| Resource | Description |
|----------|-------------|
| [ProyectoSoberana/Placa-Madre](https://github.com/ProyectoSoberana/Placa-Madre) | Repo with both KiCad projects: tester-board/ and hyperram-module/ |
| [basilisk_pcb_revc.zip](https://iis-people.ee.ethz.ch/~phsauter/basilisk/basilisk_pcb_revc.zip) | Basilisk Tester Board Rev C — original source |
| [basilisk_pcb_hyperboard_reva.zip](https://iis-people.ee.ethz.ch/~phsauter/basilisk/basilisk_pcb_hyperboard_reva.zip) | HyperRAM Daughter Board Rev A — original source |

---

## How to Contribute

This project is in its early stages. If you want to collaborate, open an issue in this repository with your area of interest: hardware, firmware, RTL synthesis, operating systems, or lithography.

---

*Proyecto Soberana — building technological independence, layer by layer.*
