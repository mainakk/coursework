# Assignment 1: constrained optimization

`ME256-HW1.ipynb` is a self-contained study notebook with model derivations,
Python implementations, solver diagnostics, and saved plots. It covers the
reciprocal objective and the fixed-area river-fence problem.

## Run

Install Python 3, then install NumPy, SciPy, Matplotlib, and JupyterLab as
described in the repository README. Open the notebook, choose a Python 3
kernel, and run all cells.

## Model and results

- The reciprocal objective is solved from three starting points. All runs
  converge to approximately `(1.139620, 1.441518)`, with objective `5.774852`.
- The river-fence model uses 50 segments, target area 25 m², and the river
  boundary `y = 8 - 0.8x`. Both branches implied by the endpoint condition are
  solved and compared. The selected fence length is approximately `4.728080 m`;
  the area and river-clearance residuals are near numerical precision.

The notebook explains the discretization and reports the conditions needed to
assess each computed result. Its study prompts include refining the fence mesh
and comparing the 35 m² case.
