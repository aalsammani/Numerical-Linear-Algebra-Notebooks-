# Contributing

Contributions are welcome. This document describes how to report issues,
suggest improvements, and submit changes.

---

## Reporting Issues

If you find an error — a wrong formula, a broken code cell, an incorrect
numerical result, or a misleading explanation — please open a GitHub issue.

A good issue report includes:

- Which file the error is in (notebook name and approximate cell, or section
  of the PDF notes).
- A clear description of what is wrong and what the correct version should be.
- For code errors: the full error message and the Python version you are using.

---

## Suggesting Improvements

Suggestions for additional topics, clearer explanations, better examples, or
missing experiments are welcome as GitHub issues with the label `enhancement`.

---

## Submitting Changes

1. Fork the repository and create a branch from `main`.
2. Make your changes.
3. If you modify a notebook, confirm that it runs top to bottom without errors
   in a clean Python environment with only the packages in `requirements.txt`.
4. If you modify the LaTeX source, confirm that it compiles with `pdflatex`
   without errors.
5. Open a pull request with a clear description of what was changed and why.

---

## Code Style

- Use `numpy`, `scipy`, and `matplotlib` only. Do not introduce other dependencies.
- Keep variable names descriptive and consistent with the mathematical notation in
  the corresponding markdown cells.
- Add a short comment to every non-obvious line of code.
- Every from-scratch implementation must be followed by a verification against
  a NumPy or SciPy reference.

---

## Mathematical Notation

Follow the conventions established in the existing notebooks:

- Matrices: uppercase italic, e.g. $A$, $Q$, $R$.
- Vectors: lowercase italic, e.g. $x$, $b$, $q_i$.
- Scalars: lowercase italic, e.g. $\sigma_i$, $\lambda$, $\varepsilon$.
- Norms: $\|x\|_2$, $\|A\|_F$, $\|A\|_2 = \sigma_{\max}(A)$.
- Machine epsilon: $\varepsilon_{\rm mach}$.
- Condition number: $\kappa(A) = \|A\|_2 \|A^{-1}\|_2 = \sigma_{\max}/\sigma_{\min}$.
