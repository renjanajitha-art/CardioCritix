# CardioCritix
**Early Detection of Cardiovascular Stress via Cardiac Criticality & ECG Complexity**

**Author:** Rejitha Renjan *(Independent Researcher | MSc Zoology)*  
**Live Interactive Prototype:** [Launch CardioCritix App](https://base44.app)  
**Status:** Research & Educational Prototype (November 2026)

---

## Overview
**CardioCritix** is a computational physiology prototype designed to detect upstream functional and metabolic stress in the cardiovascular system before irreversible structural damage—such as myocardial infarction, ventricular hypertrophy, or heart failure—appears on conventional clinical scans.

By modeling heart rate variability (HRV) and electrical conduction as a complex dynamical system operating near a critical phase transition, CardioCritix tracks how autonomic balance and cardiomyocyte bioenergetics erode under systemic load.

---

## Core Scientific Framework

### 1. Cardiac Criticality & Myocardial Negentropy
* **Cardiac Criticality:** A healthy heart does not beat like a rigid metronome; it operates near a critical boundary between strict periodicity and chaotic arrhythmia, allowing rapid autonomic adaptation to physiological demand.
* **Negentropy & Bioenergetics:** Cardiomyocytes rely on dense mitochondrial networks to sustain ATP-driven ion homeostasis. Chronic metabolic or hemodynamic stress triggers an *entropy cascade*, flattening beat-to-beat complexity.

### 2. Quantitative ECG & HRV Complexity Metrics
CardioCritix evaluates four core dynamical signatures from ECG and inter-beat (RR) interval series:
* **Shannon / Sample Entropy:** Measures beat-to-beat unpredictability and autonomic adaptability (high in healthy sinus rhythm; drops in cardiac autonomic neuropathy and heart failure).
* **Lempel-Ziv (LZ) Complexity (0–1):** Quantifies algorithmic pattern diversity across cardiac rhythms, falling as electrical dynamics become overly rigid or periodic.
* **Detrended Fluctuation Analysis (DFA $\alpha_1 / \alpha_2$):** Captures fractal long-range correlations in heart rate fluctuations; deviations from the healthy scaling range signal elevated arrhythmia risk.
* **Power-Law / $1/f$ Scaling Exponent ($\beta$):** Tracks multi-scale autonomic synchronization across sympathetic and parasympathetic branches.

---

## Stochastic Criticality Simulation Model
The interactive simulation modules model cardiac negentropy-generating capacity ($x$) against systemic hemodynamic/metabolic load ($r$) using a bistable cubic stochastic differential equation:

$$\frac{dx}{dt} = -x^3 + x + r + \sigma \xi(t)$$

* **$x$**: Myocardial negentropy-generating capacity (healthy baseline $x = 1.2$).
* **$r$**: Systemic cardiovascular load parameter (range $-0.5$ to $0.5$).
* **Critical Tipping Point ($R_{CRITICAL}$):** $\frac{2}{3\sqrt{3}} \approx 0.385$.
* **Hysteresis:** Acute, sub-threshold stress ($r < 0.385$) allows full autonomic recovery, whereas sustained overload beyond $R_{CRITICAL}$ pushes the system across a saddle-node bifurcation into decompensated cardiac failure.

---

## Application Architecture
* **Home:** Visual overview of cardiac electrophysiology, autonomic balance, and upstream metabolic stress.
* **Cardio Explorer:** Real-time bistable simulation with systemic load controls and acute perturbation ("Nudge") testing.
* **Upload & Dashboard:** ECG/HRV analysis pipeline featuring simulated clinical cohorts, complexity metric cards, spectral charts, and structural reference benchmarks.
* **Comparison:** Side-by-side hysteresis simulation contrasting reversible acute stress vs. irreversible decompensation.
* **Education:** Plain-language scientific reference guide on cardiac criticality and nonlinear HRV metrics.

**Tech Stack:** React, Tailwind CSS, Recharts, Three.js, Base44.
[![DOI](https://zenodo.org)](https://doi.org)


---

## Disclaimer
*CardioCritix is an independent research and educational prototype created for academic demonstration. All analyses and datasets are generated from synthetic simulations. It is not a medical device and must not be used for clinical diagnosis or patient care.*
