# Hardware

Knowledge base of the hardware available for the project. It is the reference for all work on
requirements, architecture, implementation and tests that depends on the hardware.

## Available hardware

| Item | Part number | Description |
|------|-------------|-------------|
| Board | NUCLEO-L476RG (PCB MB1136) | STM32 Nucleo-64 development board with on-board ST-LINK debugger |
| MCU | STM32L476RGT6 | Ultra-low-power Arm Cortex-M4F MCU, 80 MHz, 1 MB Flash, 128 KB SRAM, LQFP64 |

## Structure

| Folder | Content |
|--------|---------|
| `Boards/` | One document per board: key parameters, connectors, on-board peripherals, pin usage |
| `Components/` | One document per component (MCU, sensors, displays, modules): key parameters, interfaces, connections |
| `Datasheets/` | Source documents from manufacturers (PDF): datasheets, reference manuals, user manuals, errata, schematics |

## Reference documents

| Document | Title | File |
|----------|-------|------|
| DS10198 Rev 11 | STM32L476xx datasheet (270 pages) | `Datasheets/DS10198.pdf` |
| RM0351 Rev 11 | STM32L47x/48x/49x/4Ax reference manual (1893 pages) | `Datasheets/RM0351.pdf` |
| ES0250 Rev 13 | STM32L476xx/486xx errata sheet (65 pages) | `Datasheets/ES0250.pdf` |
| PM0214 Rev 10 | STM32 Cortex-M4 programming manual (262 pages) | `Datasheets/PM0214.pdf` |
| UM1724 Rev 17 | STM32 Nucleo-64 boards (MB1136) user manual (91 pages) | `Datasheets/UM1724.pdf` |
| MB1136 Rev C-04 | NUCLEO-L476RG board schematic (5 pages) | `Datasheets/MB1136.pdf` |

## Tool requirements

Agents read PDF documents page by page. This requires the Poppler utilities (`pdftoppm`,
`pdftotext`, `pdfinfo`) to be installed and available in `PATH`; without them only PDF files of
up to 10 pages can be read. On Windows: `winget install oschwartz10612.Poppler`.

## Rules for using and extending the knowledge base

- Component and board documents summarise the facts needed for the project; the PDF documents in
  `Datasheets/` are the authoritative source. Every value in a summary refers to the document and
  section it comes from.
- When reading a large PDF, use its table of contents and read only the relevant pages.
- New hardware is added as a document in `Boards/` or `Components/`, with its source documents
  in `Datasheets/` and a row in the tables above.
- PDF files are named by the document number (e.g. `RM0351.pdf`).
