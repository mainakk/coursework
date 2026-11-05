# ME256 Coursework: Variational Methods and Structural Optimization

Study notes and runnable reproductions of 2011 ME256 assignments. Each
notebook is designed as an end-to-end learning document, pairing a concise
problem summary with explanatory modeling notes, runnable code, and captured
outputs.

## Assignments

| Assignment | Topics | Notebook |
|---|---|---|
| Homework 1 | Constrained optimization; minimum-fence problem | [Open ME256-HW1](2011/variational-methods-structural-optimization/assignment-1/ME256-HW1.ipynb) |
| Homework 2 | Geometric reflection and refraction | [Open ME256-HW2](2011/variational-methods-structural-optimization/assignment-2/ME256-HW2.ipynb) |
| Homework 3 | Variational models for flexible wire and cloth | [Open ME256-HW3](2011/variational-methods-structural-optimization/assignment-3/ME256-HW3.ipynb) |
| Homework 4 | Functional variations; thin-plate theory; hanging chain | [Open ME256-HW4](2011/variational-methods-structural-optimization/assignment-4/ME256-HW4.ipynb) |

The official assignment statements are linked from each notebook:
[Homework 1](https://mecheng.iisc.ac.in/suresh/me256/hw2011/homework1.html),
[Homework 2](https://mecheng.iisc.ac.in/suresh/me256/hw2011/homework2.html),
[Homework 3](https://mecheng.iisc.ac.in/suresh/me256/hw2011/homework3.html),
[Homework 4](https://mecheng.iisc.ac.in/suresh/me256/hw2011/homework4.html).
The notebook summaries are not substitutes for the full statements.

## Open and run locally

Install Python 3. From the repository directory, install JupyterLab, NumPy,
SciPy, and Matplotlib, then start JupyterLab:

```text
python -m pip install jupyterlab ipykernel numpy scipy matplotlib
python -m jupyter lab
```

In JupyterLab, open one of the notebooks linked above, select a Python 3
kernel, then choose **Run → Run All Cells**. All four notebooks run with the
same Python scientific stack and contain their own explanations, executable
models, outputs, and figures.

## Reproduction notes

See each assignment README for model assumptions, numerical results, and
known limitations.

Future import and code-cleanup conventions are recorded in
[`CLEANUP-GUIDE.md`](CLEANUP-GUIDE.md) and
[`.github/copilot-instructions.md`](.github/copilot-instructions.md).
