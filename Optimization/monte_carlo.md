---
title: "Monte Carlo Simulation"
author: "Prescriptive Analytics"
date: "2024"
---

# Monte Carlo Simulation and @RISK Overview

## What is a Monte Carlo Simulation?
Monte Carlo simulation is a computational method used to model the probability of different outcomes in a process that is uncertain. It runs thousands of simulations, each time using random variables, to account for risk and variability. The method is commonly applied in finance, project management, and engineering to make informed decisions under uncertainty.

### Key Features:
- **Random Sampling**: Inputs are defined as probability distributions (e.g., normal, triangular).
- **Simulation Runs**: Thousands of simulations are executed, each with different random inputs.
- **Results**: The output is a distribution of possible outcomes, giving insights into best, worst, and most likely scenarios.

## How to Use @RISK

### 1. Define Uncertain Variables
Replace deterministic cell values in Excel with probability distributions using @RISK functions:

`=RiskNormal(mean, standard deviation)`

`=RiskTriang(min, most likely, max)`

### 2. Run a Simulation
Click **Start Simulation** in @RISK to run Monte Carlo simulations using random values drawn from the distributions defined. The software will calculate results over thousands of iterations.

### 3. Analyze Results
After the simulation, @RISK provides:
- **Histograms**: Showing the range of potential outcomes.
- **Statistics**: Key metrics such as mean, median, standard deviation, and percentiles.
- **Tornado Charts**: Sensitivity analysis that highlights which variables have the most influence on the outcomes.

### 4. Risk Percentiles
You can evaluate risks by setting thresholds (e.g., P10, P90) to determine the likelihood of exceeding or falling short of particular values.

### 5. Scenario Analysis
Adjust distributions or input assumptions to test different scenarios and observe how they affect the results.

@RISK integrates seamlessly with Excel, making it easy to perform advanced risk analysis on familiar spreadsheets.