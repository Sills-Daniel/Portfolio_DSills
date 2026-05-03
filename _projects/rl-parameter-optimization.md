---
layout: single
title: "Reinforcement Learning AI for Manufacturing Parameter Optimization"
excerpt: "Self-optimizing AI system that discovers and maintains user-specified manufacturing parameters, tested on a Nordson EFD PicoPulse inkjet printer."
date: 2026-01-09
header:
  teaser: /assets/images/projects/rl-parameter-optimization/teaser.jpg
sidebar:
  - title: "Role"
    text: "Research Engineer"
  - title: "Status"
    text: "Shipped"
  - title: "Stack"
    text: "Python · Reinforcement Learning"
toc: true
toc_label: "Contents"
---

<!-- Add teaser image: assets/images/projects/rl-parameter-optimization/teaser.jpg (575×300 px) -->

## Overview

A self-optimizing AI system for discovering and maintaining user-specified manufacturing parameters. The user defines a target parameter set, and the system autonomously learns a control policy to reach and sustain those parameters — adapting to variable environmental conditions without manual re-tuning.

## Problem Statement

Manufacturing processes like inkjet printing are sensitive to environmental variables such as temperature, humidity, and material viscosity that shift over time. Manual recalibration introduces downtime and relies on operator expertise. This system addresses that by continuously adapting to maintain process tolerances automatically.

## Approach

A reinforcement learning agent observes process feedback signals and adjusts control parameters in response. The agent is trained to minimize deviation from the user-defined target state. System development and validation were performed on a Nordson EFD PicoPulse inkjet printer.

## Stack

| Technology | Why |
|-----------|-----|
| Python | Primary implementation and model training |
| Reinforcement Learning | Enables closed-loop self-optimization without hand-coded control rules |

## Key Challenges

- Defining a reward signal that captures manufacturing tolerance compliance without over-constraining the search space
- Handling sample efficiency constraints inherent in training loops that run on physical hardware

## Outcome

Demonstrated autonomous parameter discovery and maintenance on the PicoPulse inkjet platform. The system adapts to environmental variation, reducing the need for manual operator intervention during production.

<!--
MEDIA
Teaser: assets/images/projects/rl-parameter-optimization/teaser.jpg (575×300)
Video: if you have a screen recording or demo clip, upload to YouTube/Vimeo and embed:
{% include video id="YOUR_YOUTUBE_ID" provider="youtube" %}
Or place a short local clip at: assets/videos/rl-parameter-optimization/demo.mp4
-->
