# Coursework editing instructions

When importing or revising an assignment:

- For a new coursework batch, follow the step-by-step workflow in
  `.github/agents/coursework-import.agent.md` and work on one batch at a time.
- Keep the learning material self-contained. Checked-in notebooks and
  documentation must explain the model, assumptions, run instructions, and
  results without referring to prior implementations or unavailable source
  material.
- Use the portable Python scientific stack (NumPy, SciPy, Matplotlib) for
  runnable models. Preserve the problem-solving approach, objective,
  constraints, parameter values, and meaningful variants; do not substitute
  a different algorithm for efficiency.
- Rename cryptic identifiers when their meaning is clear. Add only comments
  that clarify non-obvious modeling choices or data layouts.
- Investigate suspected formula or constraint errors. Do not silently change
  them: record the concern in the private work trace and make a correction only
  when approved. Keep corrected models and assumptions explicit in the
  notebook, without relying on historical source material.
- Keep original inputs outside the repository. Do not publish or push unless
  explicitly requested.
- For every pass, record the affected assignment, model decisions, changed
  assumptions, and unresolved questions in the private work trace.
- Run all affected notebook cells, refresh saved outputs and figures, and
  validate notebook JSON before considering the work complete.
