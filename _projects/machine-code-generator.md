---
layout: single
title: "Custom Machine Code Generator for Prototype Additive Manufacturing System"
excerpt: "Python and LabVIEW toolchain that translates standard DXF geometry into a custom machine language for a sub-0.01 mm precision motion controller in a prototype additive manufacturing platform."
date: 2026-01-08
header:
  teaser: /assets/images/projects/machine-code-generator/teaser.jpg
sidebar:
  - title: "Role"
    text: "Research Engineer — Co-Author"
  - title: "Status"
    text: "Shipped"
  - title: "Stack"
    text: "Python · LabVIEW · DXF"
  - title: "Links"
    text: "[Related paper](https://www.mdpi.com/1424-8220/23/19/8280)"
toc: true
toc_label: "Contents"
---

<!-- Add teaser image: assets/images/projects/machine-code-generator/teaser.jpg (575×300 px) -->

## Overview

Developed a Python and LabVIEW-based toolchain that reads standard DXF geometry files and produces custom machine code for a specialized motion controller integrated into a prototype additive manufacturing system. The controller achieves sub-0.01 mm positioning accuracy; this tooling bridges standard CAD workflows and the controller's non-standard instruction set, making the system programmable without hand-writing low-level commands.

## Problem Statement

The motion controller selected for the prototype system uses a proprietary instruction format that standard g-code slicers cannot produce. Manually authoring low-level code for each new geometry is error-prone and impractical for iterative research. A translator was needed that could take standard design-tool output and reliably emit correct controller instructions.

## Approach

Modified existing LabVIEW-based g-code interpreters to support nesting of the custom machine language (for high-precision operations) inside standard g-code (for coarser motion). Wrote Python programs to parse DXF geometry and emit the correct mixed-language output for the controller.

## Stack

| Technology | Why |
|-----------|-----|
| Python | DXF parsing and code generation |
| LabVIEW | Machine interface; existing g-code interpreter was LabVIEW-based |
| DXF format | Standard CAD exchange format compatible with most design tools |

## Key Challenges

- Reconciling two command languages with different coordinate systems and precision models in a single output stream
- Handling DXF geometry edge cases (arcs, polylines, nested entities) without introducing motion artifacts
- Validating generated output against physical machine behavior at sub-0.01 mm tolerance targets

## Outcome

Toolchain is in active use on the research platform. Work supported the publication: *Design, Fabrication, and Characterization of Inkjet-Printed Organic Piezoresistive Tactile Sensor on Flexible Substrate* (Sensors, 2023, 16 citations).

## Links

- [Sensors — Piezoresistive Tactile Sensor Paper](https://www.mdpi.com/1424-8220/23/19/8280)
- [Publications](/publications/)

<!--
MEDIA
Teaser: assets/images/projects/machine-code-generator/teaser.jpg (575×300)
Recommended: diagram of DXF → machine code pipeline, screenshot of tool output
-->
