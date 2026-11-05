# Assignment 2: reflections and refraction

`ME256-HW2.ipynb` is the canonical cleaned artifact. It embeds the MATLAB
transcription from `originals/2011/vmso hw2/code2.pdf`, paraphrases the tasks,
and stores output from GNU Octave 11.3.0 with `optim` 1.6.3.

## Run

Open the notebook with a Python 3 Jupyter/IPython kernel. Install GNU Octave
with its `optim` package and make `octave-cli` available on `PATH` (on Windows,
the notebook also checks the standard Program Files location). Run cells from
top to bottom. The embedded sources are written to a temporary directory for
execution and removed by the final cell; no separate reconstructed `.m` files
are required.

All six entry-point scripts completed under Octave. This indicates successful
execution, not that every computed stationary point has been independently
verified or classified as requested by the assignment. MATLAB with
Optimization Toolbox is the closer match; legacy plotting interfaces and
solver behavior can differ.

## Review notes

- The maximum-path helper `reflection_cylinder1.m` uses `x(3)` in the second
  endpoint's distance term, where `y(3)` might have been intended. The source
  version is preserved; this possible issue is not silently corrected.
- The spherical-mirror script reports signed angles as printed in the source;
  verify the sign convention against the accompanying PDF when revisiting it.
- The PDFs are the canonical record for source formatting, figures, and
  historical MATLAB output.
