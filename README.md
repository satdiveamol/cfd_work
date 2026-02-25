# Research & CFD Projects Portfolio

**Author:** Amol Satdive  
M.Tech – CFD & Turbulence Research  

This repository contains selected computational fluid dynamics (CFD) and turbulence research projects.

---

# Project 1: Rotational Control of Turbulent Pipe Flow

**Supervisor:** Prof. Ritabrata Thakur  
**Status:** Ongoing (Unpublished Work)

---

## Overview

This project investigates turbulence modification and drag reduction in fully developed pipe flow using rotational forcing.

A localized turbulent puff at Re = 1900 is evolved to Re = 5300 and simulated for 800 non-dimensional time units.

---

## Numerical Configuration

- Reynolds number (IC): **Re = 1900**
- Reynolds number (Simulation): **Re = 5300**
- Pipe radius: **R = 1**
- Pipe length: **L = 15R**
- Rotation numbers studied: **N = 0** and **N = 4**
- Bulk velocity (non-dimensional): **Ub = 0.5**

---

## Solver

Simulations performed using **OpenPipeFlow**:

- Spectral discretization (axial & azimuthal)
- High-order finite differences (radial)
- Written in Fortran 90
- MPI-parallelized for HPC

Coriolis forces added in rotating frame:

```
F_theta = -2 * Omega * u_r
F_r     =  2 * Omega * u_theta
```

This approach improves numerical stability and convergence.

---

## Key Result

For Re = 5300 and Rotation Number N = 4:

➡ Achieved **14% drag reduction**

Skin-friction coefficient evaluated as:

```
Cf = 2 * (u_tau^2) / (Ub^2)
```

---

## Flow Field Snapshots

### Initial Condition (Localized Puff – Re = 1900)
![Initial Condition](IC.png)

---

### Non-Rotating Case (N = 0)
![N0 Case](N0.png)

---

### Rotating Case (N = 4)
![N4 Case](N4.png)

---

## Modal Analysis

A custom Dynamic Mode Decomposition (DMD) framework was developed in Python to:

- Extract dominant coherent structures
- Analyze modal energy distribution
- Study stability characteristics

---

## Tech Stack

- Fortran 90  
- MPI  
- Python (NumPy, SciPy, Matplotlib)  
- HPC execution  

---

## Note

Detailed solver modifications and additional quantitative results cannot be shared at this stage as the work is unpublished.
