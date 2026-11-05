# Coursework

Documented study notes and runnable Python reproductions of historical
mechanical-engineering coursework. Materials are organized by course;
each notebook includes its own problem context, modeling assumptions,
executable code, captured results, and figures where applicable.

## Courses and assignments

### ME256: Variational Methods and Structural Optimization (2011)

| Assignment | Topics | Notebook |
|---|---|---|
| Homework 1 | Constrained optimization; minimum-fence problem | [Open ME256-HW1](variational-methods-structural-optimization/assignment-1/ME256-HW1.ipynb) |
| Homework 2 | Geometric reflection and refraction | [Open ME256-HW2](variational-methods-structural-optimization/assignment-2/ME256-HW2.ipynb) |
| Homework 3 | Variational models for flexible wire and cloth | [Open ME256-HW3](variational-methods-structural-optimization/assignment-3/ME256-HW3.ipynb) |
| Homework 4 | Functional variations; thin-plate theory; hanging chain | [Open ME256-HW4](variational-methods-structural-optimization/assignment-4/ME256-HW4.ipynb) |

The official ME256 statements are linked from each notebook:
[Homework 1](https://mecheng.iisc.ac.in/suresh/me256/hw2011/homework1.html),
[Homework 2](https://mecheng.iisc.ac.in/suresh/me256/hw2011/homework2.html),
[Homework 3](https://mecheng.iisc.ac.in/suresh/me256/hw2011/homework3.html),
[Homework 4](https://mecheng.iisc.ac.in/suresh/me256/hw2011/homework4.html).
Notebook summaries are not substitutes for the full statements.

### ME282: Computational Fluid Dynamics (2011)

- [Assignment 3: finite-difference and finite-volume methods](computational-fluid-dynamics/assignment-3/CFD-Assignment-3.ipynb)
- [Assignment 4: nine-point accuracy and iterative solvers](computational-fluid-dynamics/assignment-4/CFD-Assignment-4.ipynb)

See the [CFD course README](computational-fluid-dynamics/README.md)
for batch-specific notes and known uncertainties.

## Open and run locally

Install Python 3. From the repository directory, install JupyterLab, NumPy,
SciPy, and Matplotlib, then start JupyterLab:

```text
python -m pip install jupyterlab ipykernel numpy scipy matplotlib
python -m jupyter lab
```

In JupyterLab, open a notebook, select a Python 3 kernel, then choose
**Run → Run All Cells**. Each notebook contains its own explanations,
executable model, and captured outputs.

## Reproduction notes

See each course and assignment README for model assumptions, numerical
results, and known limitations. Repository-wide import and code-cleanup
conventions are recorded in
[`CLEANUP-GUIDE.md`](CLEANUP-GUIDE.md) and
[`.github/copilot-instructions.md`](.github/copilot-instructions.md).
