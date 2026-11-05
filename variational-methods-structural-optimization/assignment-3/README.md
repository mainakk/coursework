# Assignment 3: wire and cloth simulations

`ME256-HW3.ipynb` is a self-contained learning document with discrete model
derivations, runnable Python implementations, solver diagnostics, and saved
wire and cloth figures.

## Run

Install Python 3, then install NumPy, SciPy, Matplotlib, and JupyterLab as
described in the repository README. Open the notebook, choose a Python 3
kernel, and run all cells.

## Models and results

The wire uses one angle per segment and an exact fixed-length
parameterization. Both runs converge to an objective near `4.3472`.

The cloth minimizes displacement subject to inextensible horizontal and
vertical edges plus one diagonal per cell, forming a triangulated mesh that
can bend. A feasible folded initial mesh is used to avoid a rank-deficient
flat start. Both mesh sizes (`3 x 3` and `10 x 10` cells) converge in the
stored run; maximum edge-length errors are below `7e-11`.

These are finite-mesh numerical results. The notebook notes local-optimizer
limitations and does not claim uniqueness or convergence to a continuous
solution.
