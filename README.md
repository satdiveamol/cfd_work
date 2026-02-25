# CFD Projects Portfolio

**Author:** Amol Satdive  
M.Tech – IITD  

This repository contains selected computational fluid dynamics (CFD) related work.

---

# Project 1: Spectral decomposition of developed turbulent pipe flows

**Supervisor:** Prof. Ritabrata Thakur  
**Status:** Ongoing (Unpublished Work)

---

## Overview

The project aims to investigate turbulence control mechanisms (enhancement and suppression) in pipe
flow using various boundary forcings, for optimizing mixing or fluid transport through pipe

A localized turbulent puff at Re = 1900 is evolved to Re = 5300 and simulated for 800 non-dimensional time units.

---

## Numerical Configuration

- Reynolds number (Simulation): **Re = 5300**
- Pipe radius: **R = 1**
- Pipe length: **L = 15R**
- Rotation numbers studied: **N = 0** and **N = 4**

---

## Solver

Simulations performed using **openpipeflow**, which is an open source solver:

- Spectral discretization (axial & azimuthal)
- High-order finite differences (radial)
- Written in Fortran 90
- MPI-parallelized for HPC

To simulate rotation of the pipe, we have two approaches. If we use the inertial frame of eference, we prescribe a non-zero azimuthal velocity u_θ at R=1. However, this approach can be difficult to converge. Therefore, Coriolis forces are added when using the rotating frame of reference:

```
F_theta = -2 * Omega * u_r
F_r     =  2 * Omega * u_theta
```

This approach improves numerical stability and convergence.

---

## Flow Field Snapshots

### Initial Condition (Localized Puff, Re = 1900)
![Initial Condition](IC.png)

---

### Non-Rotating Case (N = 0)
![N0 Case](N0.png)

---

### Rotating Case (N = 4)
![N4 Case](N4.png)

---


## Key Result

- The randomness of the flow (one of the key charateristic of a turbulent flow) which can be seen in case N=0 has reduced in case N=4
- For Re = 5300 and Rotation Number N = 4:
    ➡ Achieved **14% drag reduction**

---
## Tech Stack

- Fortran 90  
- MPI  
- Python (NumPy, SciPy, Matplotlib)  
- HPC execution  

---

## Note

Detailed solver modifications and additional quantitative results cannot be shared at this stage as the work is unpublished.
