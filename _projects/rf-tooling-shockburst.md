---
layout: single
title: "RF Tooling for Enhanced Shockburst Device Analysis"
excerpt: "Open-source SDR toolset for analyzing 2.4 GHz GFSK signals on Enhanced Shockburst devices, supporting field troubleshooting and firmware validation across HackRF, Adalm Pluto, and BladeRF platforms."
date: 2026-01-08
header:
  teaser: /assets/images/projects/rf-tooling-shockburst/teaser.jpg
sidebar:
  - title: "Role"
    text: "Senior Engineer"
  - title: "Status"
    text: "Shipped"
  - title: "Stack"
    text: "Python · SDR · Embedded Systems"
toc: true
toc_label: "Contents"
---

<!-- Add teaser image: assets/images/projects/rf-tooling-shockburst/teaser.jpg (575×300 px) -->

## Overview

Developed a suite of tools for analyzing 2.4 GHz GFSK signals on Enhanced Shockburst wireless devices. The toolset measures signal strength, characterizes environmental RF noise, and demodulates radio packets — enabling engineers to troubleshoot client deployments and validate new firmware releases before field rollout.

## Problem Statement

Diagnosing wireless communication issues in Enhanced Shockburst deployments requires direct visibility into the RF environment at the protocol level. Standard spectrum analyzers capture signal presence but lack a software layer to demodulate and interpret packets. A custom, hardware-agnostic toolset was needed that could work with widely available SDR equipment.

## Approach

Built a Python-based analysis layer that interfaces with three major open-source SDR platforms: HackRF, Adalm Pluto, and BladeRF. The tool provides signal strength measurement, noise floor characterization, and GFSK demodulation for 2.4 GHz Enhanced Shockburst traffic — all from a single codebase.

## Stack

| Technology | Why |
|-----------|-----|
| Python | SDR library support; rapid iteration and scripting |
| HackRF / Adalm Pluto / BladeRF | Common, affordable open-source SDR hardware |
| GNU Radio | Signal processing pipeline for demodulation |

## Key Challenges

- Achieving reliable GFSK demodulation across varying noise environments and distances
- Supporting three distinct SDR hardware platforms from a unified codebase
- Correlating RF-layer observations with firmware-level behavior during debug sessions

## Outcome

Tool was deployed for troubleshooting live client RF communication systems and used internally for validating new firmware features before field deployment.

<!--
MEDIA
Teaser: assets/images/projects/rf-tooling-shockburst/teaser.jpg (575×300)
Recommended: screenshot of spectrum analyzer output, demodulated packet view, signal waterfall plot
-->
