# Assignment 2: reflection and refraction

`ME256-HW2.ipynb` is a self-contained study notebook with model explanations,
Python implementations, solver diagnostics, and saved figures. It includes a
circular-mirror sweep, straight and curved mirror models, two cylindrical
mirror configurations, and minimum-time refraction through a planar interface.

## Run

Install Python 3, then install NumPy, SciPy, Matplotlib, and JupyterLab as
described in the repository README. Open the notebook, choose a Python 3
kernel, and run all cells.

## Numerical results

The notebook stores the output for every model. Representative results include
a straight-mirror reflection point near `(1.24, 5.48)`, a minimum-time
refraction point near `(3.1709, 0)`, and converged minimum/maximum path
candidates for the circular and cylindrical surfaces.

The cylinder searches use a deterministic grid of starting points. Their best
converged candidates are reported, but the grid does not certify global
optimality. The assignment's second-order classification of stationary points
remains a study task.
