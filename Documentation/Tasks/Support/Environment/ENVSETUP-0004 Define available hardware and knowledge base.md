---
type: environment_setup
id: ENVSETUP-0004
title: "Define available hardware and knowledge base"
status: IN_PROGRESS
assignee: CHIEF_ENGINEER
parent:
concept:
blocked_by: []
outputs:
  - "Hardware/Hardware.md"
  - "Hardware/Datasheets/DS10198.pdf"
  - "Hardware/Datasheets/RM0351.pdf"
  - "Hardware/Datasheets/ES0250.pdf"
  - "Hardware/Datasheets/PM0214.pdf"
  - "Hardware/Datasheets/UM1724.pdf"
  - "Hardware/Datasheets/MB1136.pdf"
  - "Process/Strategy.md"
created: 2026-11-18
updated: 2026-11-18
closed:
---

# Define available hardware and knowledge base

## Scope

Define the hardware available for the project and create a hardware knowledge base that agents
can use when working on requirements, architecture, implementation and tests.

- [ ] List the available hardware (MCU board, sensors, displays, other modules) with exact part numbers
- [x] Define the location and structure of the hardware knowledge base in the documentation
- [ ] Describe each component: key parameters, interfaces, pin connections and links to datasheets
- [ ] Collect or reference datasheets and reference manuals so that agents can read them
- [x] Describe how agents use and extend the knowledge base

## Notes

- Knowledge base location: `Hardware/` (top-level folder, not under `Architecture/`), because the
  hardware description is an input for all levels, not a work product of concept tasks.
- Datasheets are stored in the repository as PDF files named by document number.
- Hardware so far: NUCLEO-L476RG board (MB1136, schematic Rev C-04) with STM32L476RGT6 MCU.
  Further components (sensors, displays, modules) are still to be added.
- Agents need Poppler (`pdftoppm`) to read PDF files longer than 10 pages; installed on the
  development machine with winget.
- Findings from the schematic for ENVSETUP-0001: HSE crystal X3 is not fitted and the ST-LINK MCO
  is disconnected for L4xxRx (SB50 open), so only internal clock sources (MSI/HSI) and the
  32.768 kHz LSE crystal (X2) are available.

## Log

- 2026-11-18 – created (status: OPEN)
- 2026-11-18 – status: OPEN → IN_PROGRESS
