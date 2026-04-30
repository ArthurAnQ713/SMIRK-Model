# SMIRK-Model
Math5421 Final Project: ODE model fitting for COVID-19 and misinformation dynamics

## Overview
This project implements the SMIRK model to study the system of disease transmission and misinformation spread. We tried to estimate four or three parameters and fit the cumulative incidence cureve in a certain period.

---

## Problem Description
We consider a compartmental model that integrates:
- Infectious disease dynamics
- Spread of misinformation

---

## Model

The system is defined by a set of ODEs:

- Disease transmission parameters: β_k, γ, μ
- Misinformation parameters: β_m, φ
- Vaccination rate: ρ

Numerical simulation is performed using `scipy.integrate.solve_ivp`.

---

## Methods

- Parameter estimation using:
  - `scipy.optimize.least_squares`
- Objective:
  - Fit cumulative cases
- Analysis:
  - Parameter identifiability (φ, λ) through profile cost

---

## Results

- Fitted parameters show:
  - Sensitivity to φ - misinformation influence
  - Identifiability issues in λ under certain conditions

- Model reproduces observed cumulative incidence curve under calibrated parameters.

---

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/ArthurAnQ713/SMIRK-Model.git
cd SMIRK-Model
```

2. Open notebooks in Jupyter:
```bash
jupyter notebook
```

3.Run the .ipynb files step by step.

---

## Dependencies

- Python 3.x
- numpy
- scipy
- matplotlib

Install:
```bash
pip install numpy scipy matplotlib
```

---

# References

- Original SMIRK model paper
- COVID-19 vaccination and case data