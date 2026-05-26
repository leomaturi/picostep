# PicoStep

PicoStep is a lightweight C++ project for exploring simple dynamical physical systems.

The goal is to build a small, clean and extensible simulation engine for toy models such as random walks, radioactive decay, diffusion, discrete fields, stochastic processes and time evolution problems.

## Core ideas

PicoStep is organized around a few basic concepts:

- `State`: the dynamic variables of the system;
- `Model`: the physical law defining the evolution;
- `Stepper`: the numerical method advancing the system;
- `Observable`: a measured quantity;
- `Simulation`: the loop orchestrating the evolution.

The project also supports field-based states and parameters, making it suitable for simple PDEs on structured grids.

## Status

Early development.