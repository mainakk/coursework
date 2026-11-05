# Coursework cleanup guide

## Reusable conventions

- Keep each notebook self-contained: state the model, assumptions, units,
  parameter choices, execution instructions, and interpretation where they are
  needed.
- Prefer the Python scientific stack (NumPy, SciPy, Matplotlib) for runnable
  numerical models.
- Preserve the original problem-solving approach and meaningful variants.
  Do not substitute a different algorithm merely to make it faster.
- Use descriptive identifiers and only the comments needed to clarify a
  non-obvious model choice or data layout.
- Investigate suspected errors, distinguish them from solver limitations, and
  record any approved correction and its effect.
- Save actual numerical output and figures in the notebook. Re-execute all
  affected cells and validate notebook JSON after edits.
- Keep original inputs outside the repository. Do not publish or push unless
  explicitly requested.

## Recorded model decisions

### Homework 1

- The reciprocal objective includes all three linear inequalities and three
  distinct initial designs. The reported optimum is supported by feasibility,
  active-constraint, and strict-convexity checks.
- The fence uses 50 equal horizontal intervals, a trapezoidal area equality,
  and river-clearance inequalities. The endpoint product condition is solved
  as its two exact alternatives, then the shorter feasible result is selected.

### Homework 2

- Reflection points are parameterized by angle on the circle and by angle and
  height on the cylinder. The cylindrical path uses the source and destination
  coordinates separately in their respective distance terms.
- The circular extrema search refines sampled local candidates over a full
  periodic interval. The cylindrical extrema search uses a deterministic
  angle-height grid and reports the best converged candidates without claiming
  global optimality.
- Refraction minimizes travel time across the planar interface and reports the
  numerical Snell-law ratio.

### Homework 3

- The wire uses one angle per segment and reconstructs its nodes from the
  fixed endpoint, preserving exact segment lengths.
- The cloth uses horizontal and vertical edges plus one diagonal per cell and
  a feasible folded start. The `3 x 3` and `10 x 10` meshes are both retained.
- Solver status, constraint residuals, and figures are stored alongside the
  code. The cloth outputs are identified as finite-mesh local-optimizer
  results.
