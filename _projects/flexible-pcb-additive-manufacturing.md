---
layout: single
title: "Additively Manufactured Multilayer Flexible PCB"
excerpt: "Additive manufacturing process for a multilayer flexible PCB demonstrating the NeXus multi-robot system. Published in ASME MSEC 2024 and the Journal of Micro and Nano Science and Engineering."
date: 2026-01-09
header:
  teaser: /assets/images/projects/flexible-pcb-additive-manufacturing/teaser.jpg
sidebar:
  - title: "Role"
    text: "Research Engineer &amp; Lead Author"
  - title: "Status"
    text: "Shipped"
  - title: "Stack"
    text: "Python · LabVIEW · PCB Design"
  - title: "Links"
    text: "[Publications](/publications/)"
toc: true
toc_label: "Contents"
---

<!-- Add teaser image: assets/images/projects/flexible-pcb-additive-manufacturing/teaser.jpg (575×300 px) -->

## Overview

Developed an additive manufacturing process for a multilayer flexible PCB that serves as the primary demonstration workpiece for the NeXus system — a prototype multi-robot manufacturing platform developed at the University of Louisville's Louisville Automation and Robotics Research Institute (LARRI). This work was published at ASME MSEC 2024 and subsequently recommended to the Journal of Micro and Nano Science and Engineering.

## Problem Statement

Demonstrating the capabilities of a novel multi-robot additive manufacturing system requires a workpiece that pushes the system across multiple tools and process steps. A multilayer flexible PCB demands precise deposition of conductive traces, dielectric layers, and component placement — making it a rigorous benchmark for automated additive workflows.

## Approach

Integrated multiple robotic and additive manufacturing tools on the NeXus platform to execute a defined process sequence: substrate preparation, conductive trace deposition, dielectric layer application, and component placement. Custom LabVIEW-based control software and Python tooling managed machine interfaces and process sequencing across the robot ensemble.

## Stack

| Technology | Why |
|-----------|-----|
| Python | Process scripting and g-code tooling |
| LabVIEW | Machine interface and motion control |
| PCB design tools | Trace layout and electrical verification |

## Key Challenges

- Coordinating multiple robots with different process speeds and positioning requirements
- Achieving consistent trace conductivity across multiple deposition passes
- Managing registration accuracy between layers on a flexible, non-rigid substrate

## Outcome

Successfully demonstrated multilayer flexible PCB fabrication on the NeXus system. Results were published at ASME MSEC 2024 (conference proceedings) and in the *Journal of Micro and Nano Science and Engineering*, Vol. 13(1), 011002 (2025).

## Links

- [Publications](/publications/)

<!--
MEDIA
Teaser: assets/images/projects/flexible-pcb-additive-manufacturing/teaser.jpg (575×300)
Recommended: photos of the completed PCB layers, video of NeXus robots in motion
Video: {% include video id="YOUR_YOUTUBE_ID" provider="youtube" %}
Or place a short local clip at: assets/videos/flexible-pcb-additive-manufacturing/demo.mp4
-->
