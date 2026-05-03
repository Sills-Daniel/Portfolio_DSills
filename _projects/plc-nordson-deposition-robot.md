---
layout: single
title: "PLC Automation System for Nordson Syringe Deposition Robot"
excerpt: "PLC-driven system that generates 1,024 unique products using a 10-bit binary counting scheme on a Nordson syringe deposition robot, with integrated UV laser curing and minimal operator intervention."
date: 2026-01-09
header:
  teaser: /assets/images/projects/plc-nordson-deposition-robot/teaser.jpg
sidebar:
  - title: "Role"
    text: "Senior Automation Engineer"
  - title: "Status"
    text: "Shipped"
  - title: "Stack"
    text: "PLC · Robotic Process Automation"
toc: true
toc_label: "Contents"
---

<!-- Add teaser image: assets/images/projects/plc-nordson-deposition-robot/teaser.jpg (575×300 px) -->

## Overview

Designed a PLC-based automation system for a Nordson syringe deposition robot that produces 1,024 unique product variants using a 10-bit binary counting scheme. The system runs batches of 8 products through a custom modular build plate, incorporates UV laser curing as a second end-effector, and requires minimal operator input — a single button press to continue after each batch.

## Problem Statement

The client needed to produce a large combinatorial product space in a repeatable, low-intervention automated process. Manually configuring each variant was not scalable; the system had to encode all variant logic into the control architecture itself.

## Approach

Implemented the 1,024-variant product space as a 10-bit binary counter in the PLC. Each count maps to a unique deposition recipe for the Nordson robot. The custom modular build plate holds 8 positions per batch; the PLC iterates through them automatically. A UV laser was integrated as a second tool and programmed for in-situ product curing between deposition steps. Users set a starting count, step direction, and press start; an alarm signals when a batch is complete.

## Stack

| Technology | Why |
|-----------|-----|
| PLC | Deterministic real-time control for robot and laser sequencing |
| Nordson syringe deposition robot | Client's existing deposition platform |
| UV laser | In-situ curing, added as second tool in this engagement |

## Key Challenges

- Mapping a 1,024-variant product space to PLC ladder logic without creating unmaintainable rungs
- Synchronizing robot deposition timing with UV laser curing dwell requirements
- Designing the modular build plate to allow batch changeovers without requiring robot re-homing

## Outcome

Delivered a fully automated system capable of unattended production across 1,024 product variants. Operator interaction reduced to three steps: set starting position, press start, acknowledge batch-complete alarm.

<!--
MEDIA
Teaser: assets/images/projects/plc-nordson-deposition-robot/teaser.jpg (575×300)
Recommended: video of automated batch run, photo of build plate with UV laser head visible
Video: {% include video id="YOUR_YOUTUBE_ID" provider="youtube" %}
Or place a short local clip at: assets/videos/plc-nordson-deposition-robot/demo.mp4
-->
