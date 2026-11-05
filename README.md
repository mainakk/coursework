# ME256 Coursework: Variational Methods and Structural Optimization

Study notes and runnable reproductions of three 2011 ME256 assignments. Each
notebook is designed as an end-to-end learning document: it summarizes the
problem in original wording, embeds the transcribed MATLAB code, and includes
captured GNU Octave output.

## Assignments

| Assignment | Topics | Notebook |
|---|---|---|
| Homework 1 | Constrained optimization; minimum-fence problem | [Open ME256-HW1](cleaned/2011/variational-methods-structural-optimization/assignment-1/ME256-HW1.ipynb) |
| Homework 2 | Geometric reflection and refraction | [Open ME256-HW2](cleaned/2011/variational-methods-structural-optimization/assignment-2/ME256-HW2.ipynb) |
| Homework 3 | Variational models for flexible wire and cloth | [Open ME256-HW3](cleaned/2011/variational-methods-structural-optimization/assignment-3/ME256-HW3.ipynb) |

The official assignment statements are linked from each notebook:
[Homework 1](https://mecheng.iisc.ac.in/suresh/me256/hw2011/homework1.html),
[Homework 2](https://mecheng.iisc.ac.in/suresh/me256/hw2011/homework2.html),
[Homework 3](https://mecheng.iisc.ac.in/suresh/me256/hw2011/homework3.html).
The notebook summaries are not substitutes for the full statements.

## Open and run locally

Install Python 3 and GNU Octave. From the repository directory, install
JupyterLab and start it:

```text
python -m pip install jupyterlab ipykernel
python -m jupyter lab
```

In JupyterLab, open one of the notebooks linked above, select a Python 3
kernel, then choose **Run → Run All Cells**. The first cell locates `octave-cli`
on `PATH`; on Windows it also checks the standard GNU Octave installation
directory. If needed, add Octave's executable directory to `PATH` before
launching JupyterLab. Assignments 1–3 require Octave's `optim` package. Install
it in Octave with:

```octave
pkg install -forge optim
```

Notebook source cells write temporary `.m` files for execution. Run the final
cleanup cell to remove them. No separate reconstructed MATLAB files are
required.

## Reproduction notes

The notebooks were tested with GNU Octave 11.3.0 and `optim` 1.6.3. Some
optimization runs do not converge, and both cloth runs fail in Octave; these
outcomes are reported rather than presented as successful solutions. See each
assignment README for details, transcription notes, and known issues. MATLAB
with Optimization Toolbox may behave differently.
