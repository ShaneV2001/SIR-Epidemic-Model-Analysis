# SIR Epidemic Model Analysis

A MATLAB implementation of the classic SIR (Susceptible-Infected-Recovered) compartmental model, used to explore how a handful of core epidemiological parameters drive the size, speed, and severity of an outbreak.

## Overview

This project models the spread of an infectious disease through a population by tracking three groups over time — the **Susceptible**, **Infected**, and **Recovered** fractions — and simulating how they shift day by day based on a small set of driving parameters. The goal was to build intuition for *why* epidemics behave the way they do: what makes one outbreak burn out quickly and another spiral, and how much leverage a factor like prior immunity really has.

## Model Parameters

The simulation is driven by a small set of variables, each explored individually to isolate its effect on outcomes:

| Parameter | Description |
|---|---|
| **β (beta)** | Transmission rate — how easily the disease spreads on contact |
| **γ (gamma)** | Recovery rate — how quickly infected individuals recover |
| **τ (tau)** | Infection length — how long an individual remains infectious |
| **R0** | Basic reproductive number — average number of new infections caused by one infected individual |
| **I0** | Initial number of infected individuals at the start of the simulation |

## What It Does

- Runs **400-day simulations** of epidemic progression and visualizes the S/I/R curves over time
- Identifies **peak infection timing** and **final attack rate** (the total share of the population ultimately infected)
- Sweeps τ, R0, and I0 individually to show how sensitive the outbreak trajectory is to each one
- Models the effect of **pre-existing population immunity**, showing how elevated prior immunity flattens and stabilizes the curve — a hands-on demonstration of the herd immunity threshold

## Key Finding

Of all the variables tested, **prior immunity level** had an outsized stabilizing effect — populations with elevated pre-existing immunity saw meaningfully dampened infection rates, even holding transmission rate constant. The model makes that relationship visible and quantifiable rather than just qualitative.

## Tech Stack

- MATLAB (core simulation and numerical integration)
- MATLAB plotting/visualization tools for S/I/R curve output

## Running It

1. Clone the repo
2. Open the main script in MATLAB
3. Adjust β, γ, τ, R0, or I0 at the top of the script to test different scenarios
4. Run — the script outputs the S/I/R plots and prints peak day / final infection rate

## Background

Built as a personal exploration of compartmental epidemic modeling, connecting to broader interests in applying quantitative/computational methods to biological systems.
