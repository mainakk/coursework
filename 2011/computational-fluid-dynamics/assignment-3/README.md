# Computational Fluid Dynamics: Assignment 3

[`CFD-Assignment-3.ipynb`](CFD-Assignment-3.ipynb) ports the recoverable
one-dimensional numerical work into a self-contained Python notebook. It
covers a Dirichlet Poisson problem, a discontinuous-coefficient diffusion
problem, the tridiagonal Thomas solver, and error studies for finite-
difference and finite-volume discretizations.

Run with Python 3, NumPy, and Matplotlib. The notebook records captured
numerical results and figures. The full problem statement was not available,
so the equations are identified from the encoded forcing and exact solutions.
It preserves the archived finite-difference interface stencil and documents
its observed non-convergence and likely coefficient discrepancy rather than
silently changing the method.
