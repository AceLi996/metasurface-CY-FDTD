# FDTD model for a single-layer metasurface CY gate

This repository contains the Ansys Lumerical FDTD modeling script
associated with the manuscript:

**High-Fidelity Single-Layer Gradient Metasurface for Optical
Quantum Controlled-Y Gate**

## File

- `CY_gate_FDTD_model.lsf`

The script constructs the metasurface geometry, material model,
input sources, boundary conditions, local mesh, and transmitted-field
monitor used in the full-wave simulations.

## Software

- Ansys Lumerical FDTD Solutions 2024 R1

## Main parameters

- Design wavelength: 1550 nm
- a-Si refractive index: 3.34443 + i5.1×10^-6
- SiO2 refractive index: 1.45
- Nanopillar dimensions: 220 nm × 400 nm × 800 nm
- Lattice period: 640 nm
- Number of PB rotation levels: 26
- Metasurface array: 26 × 26 nanopillars
- Logical-channel angle magnitude: approximately 2.669 degrees
- Local mesh size: 24 nm
- Simulation time: 1200 fs
- Boundary conditions: PML on all boundaries

## Input modes

The script contains four independently selectable circular-polarization
input modes:

1. `C_R_in`
2. `C_L_in`
3. `T_R_in`
4. `T_L_in`

The input mode is selected using the `ACTIVE_INPUT` parameter in the
script.

## Usage

1. Open Ansys Lumerical FDTD Solutions 2024 R1.
2. Create a new blank FDTD project.
3. Open and run `CY_gate_FDTD_model.lsf`.
4. Set `ACTIVE_INPUT = 0` to construct the model without running.
5. Set `ACTIVE_INPUT = 1, 2, 3, or 4` and `RUN_SIMULATION = 1`
   to simulate one physical input mode.

## Scope

This repository provides the FDTD model-construction script, including
the device geometry, materials, sources, boundary conditions, mesh, and
field monitor.

The MATLAB routines used for two-photon gate-matrix reconstruction and
fidelity evaluation are not included in this repository.

## Authors

Dongyan Li, Weihao Zhang, Yaru Li, and Guoqiang Lan.

## Contact

Questions concerning the numerical implementation may be directed to
the corresponding author.
