---
layout: single
title: "FDM 3D Print Manufacturing Automation"
excerpt: "Rebuilt a manual FDM production process to cut cycle time from 50 minutes to 12 minutes, add dual-color output, upgrade material to PCTG, and enable per-order CAD generation — all on existing hardware."
date: 2026-01-12
header:
  teaser: /assets/images/projects/fdm-manufacturing-automation/teaser.jpg
sidebar:
  - title: "Role"
    text: "Automation Engineer"
  - title: "Status"
    text: "Shipped"
  - title: "Stack"
    text: "Python · CAD · FDM 3D Printing"
toc: true
toc_label: "Contents"
---

<!-- Add teaser image: assets/images/projects/fdm-manufacturing-automation/teaser.jpg (575×300 px) -->

## Overview

Designed and implemented an automated FDM 3D printing production system for a manufacturing client. The engagement covered process optimization, material upgrades, speed improvements, and software-driven CAD customization — transforming a slow, manual, single-variant process into a high-speed, multi-variant production line without replacing the existing printer hardware.

## Problem Statement

The initial process produced one part every 50 minutes in PLA, required manual operator steps at multiple points, was limited to a single color, and could not adapt the CAD model to client specifications. Higher throughput, better chemical resistance, and per-order customization were required without adding headcount.

## Approach

Rebuilt the process around the existing Prusa 3 FDM printer with targeted changes:

- Switched from PLA to PCTG for improved chemical resistance
- Tuned print parameters for high-speed PCTG, balancing layer adhesion against cycle time
- Added dual-color print capability
- Built a Python pipeline that reads client specifications, modifies the CAD model programmatically, and regenerates the sliced g-code before each run

## Stack

| Technology | Why |
|-----------|-----|
| Python | CAD modification pipeline and print orchestration |
| PCTG filament | Superior chemical resistance compared to PLA |
| Prusa 3 FDM printer | Client's existing hardware — no capital investment required |

## Key Challenges

- PCTG requires tighter temperature and cooling control than PLA; finding the speed/quality tradeoff required iterative profiling across parameter combinations
- Programmatic CAD modification required a robust parametric model format to avoid slicing artifacts at edge-case geometry values

## Results

| Metric | Before | After |
|--------|--------|-------|
| Cycle time | 50 min | 12 min |
| Material | PLA | PCTG |
| Color options | 1 | 2 |
| Model variants | Fixed | Software-generated per spec |
| Operator steps | Multiple | Minimal |

<!--
MEDIA
Teaser: assets/images/projects/fdm-manufacturing-automation/teaser.jpg (575×300)
Recommended: before/after part photos, video of automated print cycle in action
Video: {% include video id="YOUR_YOUTUBE_ID" provider="youtube" %}
Or place a short local clip at: assets/videos/fdm-manufacturing-automation/demo.mp4
-->
