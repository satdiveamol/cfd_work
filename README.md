# Research & Computational Fluid Dynamics Projects

**Author:** Amol Satdive  
M.Tech – CFD & Turbulence Research  

This repository contains selected academic and research projects focused on
turbulence modeling, spectral simulations, flow control, and data-driven analysis.

---

# Project 1: Spectral Decomposition of Developed Turbulent Pipe Flow

**Supervisor:** Prof. Ritabrata Thakur  
**Status:** Ongoing (Unpublished Research)

## Overview

This project investigates turbulence control mechanisms in fully developed pipe flow using rotational forcing. The objective is to analyze suppression/enhancement of turbulence structures and quantify drag reduction.

---

## Numerical Configuration

- Initial condition: Localized turbulent puff at **Re = 1900**
- Simulation Reynolds number: **Re = 5300**
- Pipe radius: **R = 1**
- Pipe length: **L = 15R**
- Simulation time: **800 non-dimensional time units**
- Rotation numbers: **N = 0 and N = 4**
- Non-dimensional bulk velocity: **U_b = 0.5**

---

## Solver & Methodology

Simulations performed using the **OpenPipeFlow** solver:

- Spectral discretization (axial & azimuthal)
- High-order finite differences (radial)
- Written in **Fortran 90**
- MPI parallelized for HPC execution

Coriolis forces implemented in non-inertial rotating frame:

\[
F_\theta = -2\Omega u_r, \quad F_r = 2\Omega u_\theta
\]

This improved convergence and enabled systematic rotational studies.

---

## Key Result

For **Re = 5300** and **N = 4**:

> Achieved **14% drag reduction**

Skin-friction coefficient:

\[
C_f = \frac{2 u_\tau^2}{U_b^2}
\]

---

## Data-Driven Analysis

Developed a custom **Dynamic Mode Decomposition (DMD)** framework in Python to:

- Extract dominant coherent structures
- Compute energy spectra
- Analyze modal stability

---

# Upcoming Projects

Additional projects will be added here, including:

- [ ] Flow stability analysis
- [ ] Reduced-order modeling
- [ ] Thermal-fluid simulations
- [ ] CFD automation tools

---

# Technical Stack

- Fortran 90  
- MPI  
- Python (NumPy, SciPy, Matplotlib)  
- HPC cluster execution  

---

## Note

Detailed configurations and solver-level implementations cannot be shared at this stage as the work is unpublished.
