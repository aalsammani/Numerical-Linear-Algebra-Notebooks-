# Numerical Linear Algebra
## Theory, Algorithms, and Computation — Computational Laboratories

These Jupyter notebooks are the computational laboratories that accompany
the graduate lecture notes *Numerical Linear Algebra: Theory, Algorithms,
and Computation*. Each notebook implements the algorithms of one chapter from
scratch where that is instructive, checks every implementation against NumPy
or SciPy with tolerances derived from error bounds, and runs the experiments
that support (or delimit) the theory in the notes.

**Abdallah Alsammani, Ph.D.**
Department of Mathematical Sciences & Data Science
Delaware State University

- Lecture notes: <https://aalsammani.github.io/numerical-linear-algebra/>
- Notebook repository: <https://github.com/aalsammani/Numerical-Linear-Algebra-Notebooks>

Version 1.0, September 2026.

## Notebooks

| Chapter | Topic | Notebook | Online notes | Colab |
|---|---|---|---|---|
| 1 | Matrix computations, orthogonality, and norms: matrix products, orthogonality, norms | [`01_Matrix_Computations.ipynb`](01_Matrix_Computations.ipynb) | [notes](https://aalsammani.github.io/numerical-linear-algebra/ch01-matrix-computations/notes.html) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aalsammani/Numerical-Linear-Algebra-Notebooks/blob/main/01_Matrix_Computations.ipynb) |
| 2 | The singular value decomposition: singular value decomposition, low-rank approximation | [`02_SVD.ipynb`](02_SVD.ipynb) | [notes](https://aalsammani.github.io/numerical-linear-algebra/ch02-svd/notes.html) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aalsammani/Numerical-Linear-Algebra-Notebooks/blob/main/02_SVD.ipynb) |
| 3 | Floating-point arithmetic: ieee arithmetic, rounding, summation, cancellation | [`03_Floating_Point.ipynb`](03_Floating_Point.ipynb) | [notes](https://aalsammani.github.io/numerical-linear-algebra/ch03-floating-point/notes.html) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aalsammani/Numerical-Linear-Algebra-Notebooks/blob/main/03_Floating_Point.ipynb) |
| 4 | Conditioning and stability: condition numbers, forward and backward error | [`04_Conditioning_Stability.ipynb`](04_Conditioning_Stability.ipynb) | [notes](https://aalsammani.github.io/numerical-linear-algebra/ch04-conditioning-stability/notes.html) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aalsammani/Numerical-Linear-Algebra-Notebooks/blob/main/04_Conditioning_Stability.ipynb) |
| 5 | Gaussian elimination and LU factorization: gaussian elimination, pivoting, growth | [`05_LU.ipynb`](05_LU.ipynb) | [notes](https://aalsammani.github.io/numerical-linear-algebra/ch05-lu/notes.html) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aalsammani/Numerical-Linear-Algebra-Notebooks/blob/main/05_LU.ipynb) |
| 6 | Cholesky factorization and iterative refinement: cholesky, ldl^t, iterative refinement, condition estimation | [`06_Cholesky.ipynb`](06_Cholesky.ipynb) | [notes](https://aalsammani.github.io/numerical-linear-algebra/ch06-cholesky/notes.html) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aalsammani/Numerical-Linear-Algebra-Notebooks/blob/main/06_Cholesky.ipynb) |
| 7 | QR factorization: gram-schmidt, householder and givens qr | [`07_QR.ipynb`](07_QR.ipynb) | [notes](https://aalsammani.github.io/numerical-linear-algebra/ch07-qr/notes.html) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aalsammani/Numerical-Linear-Algebra-Notebooks/blob/main/07_QR.ipynb) |
| 8 | Linear least-squares problems: least squares, rank deficiency, regularization | [`08_Least_Squares.ipynb`](08_Least_Squares.ipynb) | [notes](https://aalsammani.github.io/numerical-linear-algebra/ch08-least-squares/notes.html) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aalsammani/Numerical-Linear-Algebra-Notebooks/blob/main/08_Least_Squares.ipynb) |
| 9 | Eigenvalues: theory and vector iterations: eigenvalue perturbation, power, inverse and rayleigh quotient iteration | [`09_Eigenvalues.ipynb`](09_Eigenvalues.ipynb) | [notes](https://aalsammani.github.io/numerical-linear-algebra/ch09-eigenvalues/notes.html) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aalsammani/Numerical-Linear-Algebra-Notebooks/blob/main/09_Eigenvalues.ipynb) |
| 10 | The QR algorithm: hessenberg reduction, shifted qr algorithm, svd computation | [`10_QR_Algorithm.ipynb`](10_QR_Algorithm.ipynb) | [notes](https://aalsammani.github.io/numerical-linear-algebra/ch10-qr-algorithm/notes.html) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aalsammani/Numerical-Linear-Algebra-Notebooks/blob/main/10_QR_Algorithm.ipynb) |
| 11 | Sparse matrices and Krylov subspace methods: sparse matrices, arnoldi, gmres, cg, preconditioning | [`11_Krylov_Methods.ipynb`](11_Krylov_Methods.ipynb) | [notes](https://aalsammani.github.io/numerical-linear-algebra/ch11-krylov/notes.html) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aalsammani/Numerical-Linear-Algebra-Notebooks/blob/main/11_Krylov_Methods.ipynb) |
| 12 | Randomized numerical linear algebra: random embeddings, randomized svd, sketching | [`12_Randomized_Numerical_Linear_Algebra.ipynb`](12_Randomized_Numerical_Linear_Algebra.ipynb) | [notes](https://aalsammani.github.io/numerical-linear-algebra/ch12-randomized/notes.html) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aalsammani/Numerical-Linear-Algebra-Notebooks/blob/main/12_Randomized_Numerical_Linear_Algebra.ipynb) |

The notebooks are companions to the notes, not a substitute for them: the
definitions, theorems, proofs and exercises are in the notes, and every
reference in a notebook ("Theorem 5.3", "(7.1)", "Exercise 8.4") links to the
corresponding place in the online notes. Several chapters of the notes also
have case-study notebooks on public data; those are available on the website.

## Prerequisites

Undergraduate linear algebra, basic analysis, and Python with NumPy (writing
functions, loops and array operations). No previous course in numerical
analysis is assumed.

## Installation

Python 3.11 or newer is required. The notebooks were tested with Python
3.14.3, NumPy 2.5.3, SciPy 1.18.1 and Matplotlib 3.11.2 on Windows 11; other
versions satisfying `requirements.txt` are expected to work but were not
tested.

With pip and a virtual environment (from the repository folder):

```bash
# macOS / Linux
python3 -m venv .venv
source .venv/bin/activate

# Windows (PowerShell)
py -m venv .venv
.venv\Scripts\Activate.ps1

# then, on every system
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

With conda (not part of the tested setup):

```bash
conda env create -f environment.yml
conda activate nla-notebooks
```

## Running the notebooks

Start JupyterLab from the repository folder and open a notebook:

```bash
jupyter lab
```

Each notebook is self-contained: run it from top to bottom in a fresh kernel
(*Kernel > Restart Kernel and Run All Cells*). The notebooks do not depend on
each other and can be run in any order. The saved outputs were produced by
exactly this procedure.

**Google Colab.** The Colab links in the table open the notebooks directly
from this repository. NumPy, SciPy and Matplotlib are preinstalled on Colab,
so no installation is needed. The Chapter 12 notebook downloads its dataset
from this repository automatically when the `data/` folder is not present.

## Datasets

Only the Chapter 12 notebook reads a data file: `data/ascent.npz`, the
512 x 512 grayscale photograph distributed by SciPy as
`scipy.datasets.ascent()`, derived from a public-domain (CC0) photograph.
`data/README.md` documents its source, checksums and processing. All other
experiments use matrices generated in the notebooks.

## Reproducibility

Every random experiment uses a NumPy `Generator` with a fixed seed, so the
printed numbers are reproducible on a given machine. Quantities that are of
the size of rounding errors (for example a loss of orthogonality of about
$10^{-15}$) can differ in their last digits between processors and BLAS/LAPACK
libraries, and the notebooks' checks allow for this with tolerances derived
from error bounds. Run times are observations on the machine that executed
the notebook and are labeled as such; the machine-independent measures of cost
are the flop counts discussed in the notes.

## Citation

If you use these notebooks, please cite them (see `CITATION.cff`):

> Abdallah Alsammani. *Numerical Linear Algebra: Theory, Algorithms, and
> Computation — Computational Laboratories*, version 1.0, 2026.
> https://github.com/aalsammani/Numerical-Linear-Algebra-Notebooks

## License

The notebooks are released under the MIT License (see `LICENSE`). The dataset
in `data/` keeps the terms of its source, described in `data/README.md`.
Corrections and suggestions are welcome through the repository's issue
tracker.
