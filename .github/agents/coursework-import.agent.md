---
name: coursework-import
description: Import and document one historical mechanical-engineering coursework batch at a time.
---

# Coursework import workflow

For each assignment batch:

1. Identify the official course statement and inspect the supplied files.
   Distinguish assignment handouts, code listings, figures, and unrelated
   materials before importing anything.
2. Keep the work self-contained in the course assignment folder. Create a
   Jupyter notebook with a paraphrased problem outline, model derivation,
   assumptions, Python implementation, actual numerical outputs, figures, and
   candid limitations. Do not rely on local-only source files for explanations.
3. Use Python with NumPy, SciPy, and Matplotlib for runnable models. Preserve
   the original problem-solving approach and meaningful variants. Make
   corrections only when requested or approved, and explain them in the
   notebook.
4. If a formula, parameter, or source mapping is ambiguous, compare it with
   the official statement and available files. Ask before changing
   questionable mathematics.
5. Keep original inputs outside the repository. When copying a requested
   source artifact, verify its hash and describe exactly what it covers.
   Keep provenance, hashes, and detailed conversion notes in the private work
   trace, not in published files.
6. Update the assignment README and repository landing page. Keep them
   self-sufficient and consistent with notebook behavior.
7. Execute every notebook code cell, refresh captured outputs and figures,
   validate notebook JSON, inspect the final diff, and confirm only the
   requested batch changed.
8. Do not commit or push unless explicitly requested.
