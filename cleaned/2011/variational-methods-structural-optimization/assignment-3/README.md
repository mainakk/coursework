# Assignment 3: wire and cloth simulations

`ME256-HW3.ipynb` is the canonical cleaned artifact. It embeds both MATLAB
source variants, paraphrases the assignment, and records GNU Octave output.

The two source folders, `originals/2011/vmso3/` and
`originals/2011/vmso31/`, contain distinct code and image PDFs. Matching
filenames do not mean identical versions; each transcription is kept in its
own directory.

## Run and results

Open the notebook with a Python 3 Jupyter/IPython kernel. Install GNU Octave
with its `optim` package and make `octave-cli` available on `PATH` (on Windows,
the notebook also checks the standard Program Files location). Run cells from
top to bottom. Embedded source cells write temporary `.m` files for execution;
the final cell removes them.

In Octave 11.3.0, both wire scripts reach the 100-iteration limit with exit
flag 0, so they have not converged. Both cloth scripts fail in `fmincon` with a
singular-matrix warning and “could not regain binding constraints.” These
results are reported as failures, not treated as successful solutions. The
original methods and constraints are retained; compare with MATLAB and the
source PDFs before drawing further conclusions.

## Version difference to review

Both PDFs contain the wire simulation and cloth simulation. `vmso3` initializes
the cloth with `n = 3` and constrains horizontal edges, vertical edges, and
both diagonals of each cell. `vmso31` uses `n = 10`; its `dist.m` contains the
horizontal-edge and diagonal constraints but no vertical-edge loop. This
difference is retained exactly as a version distinction, not repaired.
