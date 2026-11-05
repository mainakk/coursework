# Assignment 1

`ME256-HW1.ipynb` is the canonical cleaned artifact. It embeds the MATLAB
transcription from `originals/2011/VMSO_assignment1/codes.pdf`, paraphrases the
assignment, and stores the output from GNU Octave 11.3.0 with `optim` 1.6.3.

## Run

Open the notebook with a Python 3 Jupyter/IPython kernel. Install GNU Octave
with its `optim` package and make `octave-cli` available on `PATH` (on Windows,
the notebook also checks the standard Program Files location). Run cells from
top to bottom. Embedded source cells write temporary `.m` files, execute them,
and the final cell removes those files. No separate reconstructed `.m` files
are required.

## Results and transcription notes

- The reciprocal-objective runs complete from all three initial points.
- Octave's river-fence run reaches its 100-iteration limit with exit flag 0
  and a constraint violation of about 0.119; it is not a converged result.
- The reciprocal contour has singularities at zero and produces nonfatal
  plotting warnings.
- The PDF identifies the river-fence entry script only as `Untitled3.m`; it is
  embedded as `river_fence.m`. The formulations, solver, and starting values
  are retained. The source's `Title` command is normalized to `title`.
- MATLAB with Optimization Toolbox is the closer match to the historical
  runtime. The notebook's captured results are from Octave, not MATLAB.
