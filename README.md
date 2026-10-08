# Pandemic Resource Planning Using Stochastic Demand Modelling and the Newsvendor Model

## Project Overview

This project investigates a mathematical and computational approach to pandemic resource planning under uncertain demand.

The analysis combines:

- Deterministic demand modelling
- Stochastic demand simulation
- Demand uncertainty analysis
- Newsvendor optimisation
- Sensitivity analysis
- Computational visualisation

The objective is to examine how uncertainty in resource demand can influence planning decisions and how underage and overage costs can be incorporated into resource allocation.

## Problem Statement

Pandemic resource planning involves making decisions about resource requirements when future demand is uncertain.

Planning for too little capacity can result in shortages, while planning for excessive capacity can result in underutilised resources and additional costs.

This project uses stochastic demand modelling and the Newsvendor framework to examine this trade-off.

## Methodology

The analysis follows a structured workflow:

1. Develop a deterministic baseline demand model.
2. Combine pathogen-induced and worried-well demand components.
3. Introduce uncertainty around the deterministic demand.
4. Generate stochastic demand scenarios.
5. Analyse the resulting demand distributions.
6. Apply Newsvendor optimisation.
7. Evaluate the recommended planning quantity.
8. Perform computational and sensitivity analysis.

## Stochastic Demand Modelling

The deterministic demand is represented as:

\[
D_t = I_{p,t} + I_{w,t}
\]

where:

- `Ip` represents the pathogen-induced demand component.
- `Iw` represents the worried-well demand component.

The model introduces a relative uncertainty parameter of 15% and generates 1,000 stochastic scenarios for each demand observation.

The simulations use normally distributed random shocks and constrain negative demand values to zero.

## Key Results

The deterministic simulation covered **351 days** of case-study data.

The maximum deterministic combined demand was approximately **0.8340**, occurring on Day 8.

For the peak-demand day:

- Deterministic demand: **0.8340**
- Mean stochastic demand: **0.8353**
- Median stochastic demand: **0.8385**
- Standard deviation: **0.1260**
- Minimum simulated demand: **0.4020**
- Maximum simulated demand: **1.1891**

The stochastic scenarios demonstrate how uncertainty can produce both lower-than-baseline and higher-than-baseline demand outcomes.

## Newsvendor Optimisation

The Newsvendor model evaluates the trade-off between:

- **Underage cost** — the consequence of planning for insufficient resources.
- **Overage cost** — the consequence of planning for excessive resources.

The calculated critical fractile in the analysis is **0.80**, representing an 80% demand-coverage level for the recommended planning quantity.

## Visual Analysis

The project includes visualisations covering:

- Pathogen-induced and worried-well populations
- Combined healthcare demand
- Worried-well to pathogen-induced demand ratio
- Stochastic demand trajectories
- Stochastic demand distributions
- Demand distributions across selected days
- Newsvendor optimisation and sensitivity analysis

## Tools & Techniques

**Modelling & Analysis**
- Python
- Mathematical modelling
- Stochastic simulation
- Statistical analysis
- Optimisation

**Visualisation**
- Matplotlib
- Computational plots

**Concepts**
- Demand uncertainty
- Monte Carlo-style scenario generation
- Newsvendor model
- Critical fractile
- Underage and overage costs
- Sensitivity analysis

## Key Learning

This project demonstrates how deterministic estimates can be extended into stochastic scenarios to support decision-making under uncertainty.

It also demonstrates the importance of considering the cost of both underestimating and overestimating demand when determining a planning quantity.

## Limitations

The model is based on the assumptions and parameters specified in the underlying case study.

The stochastic demand analysis uses a 15% relative uncertainty assumption and 1,000 scenarios per demand observation. Results should therefore be interpreted within the modelling assumptions rather than as forecasts of real-world pandemic demand.

## Project Status

Completed analytical project.

## Disclaimer

This repository documents an analytical and modelling project for educational and portfolio purposes. The results are dependent on the assumptions, parameters and data used in the analysis.
