<p align="center">
  <img src="https://raw.githubusercontent.com/ProyectoSoberana/soberana/main/logo.svg" width="350" alt="Proyecto Soberana">
</p>

# Proyecto Soberana

> **English:** Proyecto Soberana is a long-term initiative to build a fully independent technology stack — from processor design and lithography to the operating system running on top. The goal is complete sovereignty over every layer of the hardware and software stack. As a matter of principle, this project is conducted in Spanish. [Read in English →](README.en.md)

---

**Soberanía tecnológica desde el silicio hasta el sistema operativo.**

Proyecto Soberana es una iniciativa de largo plazo orientada a construir una pila tecnológica completamente independiente: desde el diseño del procesador y la placa madre hasta el sistema operativo que corre sobre ellos. El objetivo final es no depender de ningún proveedor externo en ninguna capa del stack de hardware o software.

---

## Motivación

La dependencia tecnológica es una forma de dependencia geopolítica. Cada CPU importado, cada sistema operativo propietario y cada capa de firmware opaca representa un vector de control externo. Proyecto Soberana busca revertir eso construyendo, capa por capa, una alternativa completamente auditada, reproducible y de código/hardware abierto.

---

## Hoja de ruta

| Etapa | Descripción | Estado |
|-------|-------------|--------|
| 1 | Enviar diseño Basilisk a IHP para fabricación del procesador en 130nm BiCMOS | 📋 Planificado |
| 2 | Fabricar placa madre (Basilisk Tester Board Rev C) y módulo HyperRAM (Rev A) — JLCPCB / PCBWay | 📋 Planificado |
| 3 | Ensamblar: soldar chip Basilisk a la placa madre y conectar módulo HyperRAM — validar funcionamiento | 📋 Planificado |
| 4 | Instalar Linux sobre el hardware soberano | 📋 Planificado |
| 5 | Desarrollar placa madre y módulo HyperRAM con empresa nacional argentina | 📋 Planificado |
| 6 | Adquirir sistema de litografía 130nm propio (KrF — IHP BiCMOS PDK) | 📋 Planificado |
| 7 | Producir chips soberanos con litografía propia | 📋 Planificado |

---

## Filosofía

- **Abierto por diseño:** todo el trabajo es open-source y reproducible.
- **Incremental:** cada etapa es funcional por sí misma y base de la siguiente.
- **Documentado:** cada decisión técnica queda registrada para que cualquiera pueda replicar el proceso.
- **Independiente:** sin dependencias de licencias propietarias donde sea evitable.

---

## Arquitectura de la pila tecnológica

```
┌─────────────────────────────────┐
│        Sistema Operativo        │  ← FreeBSD / Linux RISC-V
├─────────────────────────────────┤
│   Firmware (OpenSBI + U-Boot)   │  ← Stack de arranque
├─────────────────────────────────┤
│     SoC Basilisk (CVA6 RV64)    │  ← Chip fabricado en IHP 130nm
├─────────────────────────────────┤
│         Placa Madre             │  ← Basilisk Tester Board (KiCad)
├─────────────────────────────────┤
│       Módulo HyperRAM           │  ← Daughter board Rev A
└─────────────────────────────────┘
```

---

## Referencias

### Procesador — SoC Basilisk

| Recurso | Link |
|---------|------|
| Página del proyecto Basilisk (ETH Zürich) | https://iis-people.ee.ethz.ch/~phsauter/basilisk/ |
| Diseño RTL + flow IHP 130nm (upstream) | https://github.com/pulp-platform/cheshire-ihp130-o |
| Diseño RTL + flow IHP 130nm (fork Soberana) | https://github.com/ProyectoSoberana/cheshire-ihp130-o |
| GDS listo para enviar a IHP (output del flow, sin recompilar) | https://iis-people.ee.ethz.ch/~tbenz/gds/basilisk_release.gds.gz |
| Plataforma base Cheshire | https://github.com/pulp-platform/cheshire |
| PDK IHP Open Source | https://github.com/IHP-GmbH/IHP-Open-PDK |

### Placa madre y módulo HyperRAM — KiCad

| Recurso | Descripción |
|---------|-------------|
| [ProyectoSoberana/Placa-Madre](https://github.com/ProyectoSoberana/Placa-Madre) | Repo con ambos proyectos KiCad: tester-board/ y hyperram-module/ |
| [basilisk_pcb_revc.zip](https://iis-people.ee.ethz.ch/~phsauter/basilisk/basilisk_pcb_revc.zip) | Basilisk Tester Board Rev C — fuente original |
| [basilisk_pcb_hyperboard_reva.zip](https://iis-people.ee.ethz.ch/~phsauter/basilisk/basilisk_pcb_hyperboard_reva.zip) | HyperRAM Daughter Board Rev A — fuente original |

---

## Cómo contribuir

Este proyecto está en sus etapas iniciales. Si querés colaborar, abrí un issue en este repositorio con tu área de interés: hardware, firmware, síntesis RTL, sistemas operativos o litografía.

---

*Proyecto Soberana — construyendo independencia tecnológica, capa por capa.*
