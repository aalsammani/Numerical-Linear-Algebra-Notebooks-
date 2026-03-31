# Numerical Linear Algebra — PhD Course Materials

A complete set of lecture notes and computational notebooks for a PhD-level course in
Numerical Linear Algebra. The materials pair rigorous mathematical derivations with
hands-on Python implementations, making every algorithm concrete and verifiable.

---

## Contents

| File | Description |
|---|---|
| `numerical_linear_algebra_notes.pdf` | Complete LaTeX lecture notes (compiled PDF) |
| `numerical_linear_algebra_notes.tex` | LaTeX source for the lecture notes |
| `01_Fundamentals.ipynb` | Matrix multiplication · Orthogonal matrices · Norms · SVD |
| `02_QR_Least_Squares.ipynb` | Projections · QR factorization · Gram-Schmidt · Householder · Least squares |
| `03_Conditioning_Stability.ipynb` | Condition numbers · Floating-point arithmetic · Stability |
| `04_Systems_of_Equations.ipynb` | Gaussian elimination · Pivoting · Cholesky factorization |
| `05_Eigenvalues.ipynb` | Eigenvalue algorithms · Hessenberg reduction · Rayleigh quotient · QR algorithm · SVD connection |

---

## Lecture Notes (PDF)

The PDF provides a self-contained written reference for the entire course. Each section
opens with precise definitions and theorems, followed by algorithmic remarks and numerical
observations. The notes are structured to accompany the notebooks: every topic treated
computationally in a notebook has its theoretical foundation in the PDF.

To recompile from source:

```bash
pdflatex numerical_linear_algebra_notes.tex
pdflatex numerical_linear_algebra_notes.tex   # run twice for cross-references
```

Required LaTeX packages: `amsmath`, `amssymb`, `amsthm`, `geometry`, `enumitem`,
`booktabs`, `microtype`, `hyperref`. All are included in a standard TeX Live or MiKTeX
installation.

---

## Jupyter Notebooks

### Design Principles

Each notebook follows a consistent structure for every topic:

1. **Motivation** — why this algorithm or concept matters computationally
2. **Mathematical foundation** — precise definitions, key theorems, and formulas in LaTeX
3. **Algorithmic discussion** — cost, stability, and comparison with alternatives
4. **From-scratch implementation** — educational Python code following the algorithm directly
5. **Library comparison** — verification against NumPy or SciPy
6. **Numerical experiments** — experiments designed to reveal the behavior described by theory
7. **Interpretation** — explicit discussion of what the output shows

The notebooks are not a code dump. They read as a computational textbook with theory and
computation tightly connected.

### Notebook Summaries

#### 01 — Fundamentals

Covers the building blocks that all subsequent algorithms depend on.

- **Matrix multiplication**: triple-loop derivation, outer-product (rank-1 sum) view,
  block multiplication, and a timing comparison that demonstrates the BLAS speed gap
  (10 000x over a naive Python loop for n = 200).
- **Orthogonal matrices**: algebraic properties verified numerically, rotation and
  Householder reflector geometry visualized.
- **Norms**: vector p-norms and induced matrix norms, Frobenius norm, equivalence bounds,
  and a Monte Carlo demonstration that the 2-norm equals the maximum amplification over
  the unit sphere.
- **SVD**: full and thin decomposition, outer-product reconstruction, Eckart-Young best
  rank-k approximation theorem, and all four Moore-Penrose pseudoinverse conditions.

#### 02 — QR Factorization and Least Squares

Covers the algorithms used to solve overdetermined systems and to orthogonalize bases.

- **Projections**: orthogonal projector construction, idempotency and symmetry verified,
  residual orthogonality demonstrated geometrically.
- **QR factorization**: full vs thin QR, reconstruction and orthogonality errors.
- **Gram-Schmidt**: classical and modified Gram-Schmidt from scratch; orthogonality loss
  experiment across condition numbers from 10^2 to 10^14 showing how CGS degrades while
  Householder remains near machine epsilon.
- **Householder triangularization**: sign-corrected reflector construction, QR via
  successive reflections.
- **Least squares**: normal equations, QR approach, and SVD approach compared on an
  ill-conditioned problem (kappa ~ 10^8); perturbation box plots showing why the normal
  equations are unreliable at high condition numbers.

#### 03 — Conditioning and Stability

The conceptual core of the course: separating problem sensitivity from algorithm quality.

- **Condition numbers**: Hilbert matrix kappa growing to 10^16 by n = 12; perturbation
  experiment showing amplification matching the theoretical bound; geometric interpretation
  as the ratio of ellipse semi-axes.
- **Floating-point arithmetic**: machine epsilon derived from first principles; catastrophic
  cancellation in sqrt(x+1) - sqrt(x), the quadratic formula, exp(x)-1, and log(1+x);
  numerically stable reformulations using expm1 and log1p.
- **Stability**: backward and forward error decomposition; Wilkinson matrix demonstrating
  the difference between an unstable algorithm and an ill-conditioned problem; QR vs
  normal equations on the same ill-conditioned least squares problem.

#### 04 — Systems of Equations

Direct factorization methods for square and symmetric positive definite systems.

- **Gaussian elimination**: LU from scratch with forward and back substitution, verified
  against SciPy.
- **Pivoting**: partial pivoting LU from scratch; Wilkinson matrix growth factor reaching
  2^(n-1) without pivoting; growth factor vs n plot.
- **Cholesky**: factorization from scratch with SPD detection; solve via triangular
  systems; timing comparison against LU showing the expected 2x speedup.

#### 05 — Eigenvalues

Iterative algorithms for computing eigenvalues and their connection to the SVD.

- **Eigenvalue problems**: symmetric (eigh) vs nonsymmetric (eig) computation; Schur
  decomposition; Ginibre random matrix eigenvalue distribution.
- **Hessenberg reduction**: scipy hessenberg, structure visualized; tridiagonal case for
  symmetric matrices.
- **Rayleigh quotient**: quadratic accuracy confirmed by log-log slope measurement (2.007
  vs theoretical 2.0); Rayleigh Quotient Iteration with cubic convergence.
- **QR algorithm**: unshifted QR from scratch; Wilkinson-shifted QR comparison (93 vs
  447 iterations, 4.8x speedup).
- **Other algorithms**: power iteration, inverse iteration with LU prefactorization;
  SVD via eigenvalues of A^T A (condition squaring demonstrated) and via the augmented
  symmetric matrix [[0, A^T], [A, 0]].

---

## Requirements

Python 3.9 or later is required. All dependencies are standard scientific Python:

```
numpy>=1.24
scipy>=1.10
matplotlib>=3.7
```

Install with:

```bash
pip install -r requirements.txt
```

No other libraries are needed. The notebooks deliberately avoid obscure dependencies.

---

## Running the Notebooks

Clone the repository and launch Jupyter:

```bash
git clone https://github.com/<your-username>/numerical-linear-algebra.git
cd numerical-linear-algebra
pip install -r requirements.txt
jupyter notebook
```

Open any of the five notebooks. Each notebook is fully self-contained and runs top to
bottom without any external data files or prior notebook state.

If you prefer JupyterLab:

```bash
pip install jupyterlab
jupyter lab
```

---

## Audience and Prerequisites

These materials are written for PhD students in mathematics, applied mathematics,
statistics, and computational science. The assumed background is:

- Linear algebra at the level of a strong undergraduate course (vector spaces,
  eigenvalues, inner products)
- Basic Python and NumPy familiarity
- Some exposure to mathematical analysis (limits, continuity, norms)

The materials do not assume prior knowledge of numerical methods or floating-point
arithmetic.

---

## Course Topics at a Glance

| Topic | Key algorithms | Key concepts |
|---|---|---|
| Matrix multiplication | Block GEMM | Rank-1 outer product view, O(n^3) cost |
| Orthogonal matrices | QR via Householder | Norm preservation, stability |
| Norms | — | Induced 2-norm = sigma_max, Frobenius norm |
| SVD | Golub-Reinsch (via NumPy) | Eckart-Young, pseudoinverse |
| Projections | — | P^2 = P = P^T, residual orthogonality |
| QR factorization | Householder, Gram-Schmidt | Full vs thin QR |
| Gram-Schmidt | CGS, MGS | Loss of orthogonality |
| Least squares | Normal equations, QR, SVD | Condition number squaring in normal equations |
| Condition numbers | — | kappa = sigma_max / sigma_min |
| Floating-point | — | eps_mach, catastrophic cancellation |
| Stability | — | Backward error, forward error |
| Gaussian elimination | LU | O(2n^3/3), growth factor |
| Pivoting | Partial pivoting | Wilkinson matrix, stability |
| Cholesky | — | SPD, O(n^3/3), unconditional stability |
| Eigenvalues | QR algorithm, power/inverse iteration | Schur form, shifts |
| Hessenberg reduction | Householder similarity | O(10n^3/3), Hessenberg invariance |
| Rayleigh quotient | Rayleigh Quotient Iteration | Quadratic accuracy, cubic convergence |
| QR algorithm | Unshifted and Wilkinson-shifted | Convergence rate, deflation |
| SVD via eigenvalues | Augmented symmetric matrix | kappa(A^T A) = kappa(A)^2 |

---

## References

- L. N. Trefethen and D. Bau III, *Numerical Linear Algebra*, SIAM, 1997.
- G. H. Golub and C. F. Van Loan, *Matrix Computations*, 4th ed., Johns Hopkins University Press, 2013.
- N. J. Higham, *Accuracy and Stability of Numerical Algorithms*, 2nd ed., SIAM, 2002.
- J. W. Demmel, *Applied Numerical Linear Algebra*, SIAM, 1997.

---

## License

This work is released under the MIT License. See `LICENSE` for details.
