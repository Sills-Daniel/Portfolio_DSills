---
layout: single
title: "Wireless Underwater Robot Prototype"
excerpt: "Underwater robot controllable via pre-programmed autonomous routines or radio link, built from a mix of off-the-shelf electronics and custom 3D-printed and laser-cut structural parts."
date: 2026-01-09
header:
  teaser: /assets/images/projects/underwater-robot/teaser.jpg
sidebar:
  - title: "Role"
    text: "Research Engineer"
  - title: "Status"
    text: "Shipped"
  - title: "Stack"
    text: "Arduino · Raspberry Pi · CAD"
toc: true
toc_label: "Contents"
---

<!-- Add teaser image: assets/images/projects/underwater-robot/teaser.jpg (575×300 px) -->

## Overview

Designed, built, and tested an underwater robot capable of operating in two modes: autonomous execution of pre-programmed movement routines, and manual control via radio communication. The physical structure was designed from scratch and fabricated by combining commercial off-the-shelf components with custom parts produced by FDM 3D printing and laser cutting.

## Problem Statement

Underwater robot platforms are expensive and typically purpose-built for narrow use cases. A prototype was needed to validate control concepts in an aquatic environment at low cost, using components that could be iterated on quickly without long lead times or specialized tooling.

## Approach

Designed the physical structure from first principles, accounting for buoyancy, waterproofing, thruster placement, and control surface geometry. Custom structural parts were modeled in CAD and fabricated via FDM printing and laser cutting. Electronics were built around Arduino (low-level motor and sensor control) and Raspberry Pi (higher-level logic and wireless interface), with radio modules handling the remote control link.

## Stack

| Technology | Why |
|-----------|-----|
| Arduino | Real-time motor and sensor control |
| Raspberry Pi | Higher-level logic and wireless communication |
| CAD (3D modeling) | Custom structural parts designed for rapid iteration |
| FDM 3D printing / laser cutting | Low-cost, fast-turnaround custom part fabrication |

## Key Challenges

- Waterproofing the electronics enclosure while keeping the assembly accessible for iterative modifications
- Balancing buoyancy and weight distribution with the constraint of custom-fabricated parts whose mass was determined after modeling
- Achieving reliable radio link performance at the air-water interface

## Outcome

Prototype successfully demonstrated both autonomous routine execution and radio-controlled operation in aquatic testing. The project validated a hybrid fabrication approach — off-the-shelf electronics plus custom structural parts — as a practical path for rapid underwater robot prototyping.

<!--
MEDIA
Teaser: assets/images/projects/underwater-robot/teaser.jpg (575×300)
Recommended: photos of the assembled robot, video of it operating underwater
Video: {% include video id="YOUR_YOUTUBE_ID" provider="youtube" %}
Or place a short local clip at: assets/videos/underwater-robot/demo.mp4
-->
