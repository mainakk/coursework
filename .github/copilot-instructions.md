# Coursework cleanup instructions

When importing another assignment into this repository:

- Treat the source PDFs/files as authoritative and leave them unchanged.
- Preserve the original problem-solving approach, equations, constraints,
  parameter values, solver choices, and distinct historical variants. Do not
  implement algorithmic improvements during a readability pass.
- Make cleaned learning material self-contained in the assignment notebook:
  embed runnable source and store actual runtime output. Keep generated source
  files temporary.
- Rename cryptic identifiers when their meaning is clear from the code or
  source material. Prefer physical meanings such as coordinates, lengths,
  bounds, objective values, and optimizer results. Retain mathematical symbols
  when they directly match an equation, and retain names required by MATLAB or
  Octave callback interfaces.
- Add only brief comments needed to explain a non-obvious model, packed data
  layout, callback requirement, or preserved anomaly. Do not annotate obvious
  statements.
- Do not silently fix suspicious formulas or constraints. Preserve them and
  record the concern for review; place proposed alternatives in a separate
  note or variant.
- Record every cleanup pass in `CLEANUP-GUIDE.md`: list changed notebook/source
  cells, identifier renames, comments added, and unresolved concerns. Update
  the reusable conventions there when the process changes.
- Re-run the affected notebook code with the documented runtime after edits.
  Refresh stored outputs, accurately label optimizer failures and
  non-convergence, and validate notebook JSON and embedded-source completeness.
