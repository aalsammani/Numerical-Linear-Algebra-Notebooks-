# Data

## `ascent.npz` — "Ascent" photograph (used by `12_Randomized_Numerical_Linear_Algebra.ipynb`)

- **Content:** one array, `image`, of type `uint8` and shape `(512, 512)`;
  entries are gray levels from 0 (black) to 255 (white).
- **Source:** the image distributed by SciPy as `scipy.datasets.ascent()`,
  file <https://raw.githubusercontent.com/scipy/dataset-ascent/main/ascent.dat>.
  The SciPy documentation states that it is derived from the photograph
  <https://pixnio.com/people/accent-to-the-top>, which that site lists as CC0
  (public domain).
- **Integrity:** the SHA-256 checksum of the upstream `ascent.dat` is
  `03ce124c1afc880f87b55f6b061110e2e1e939679184f5614e38dacc6c1957e2`, the value
  recorded in `scipy.datasets`. The SHA-256 checksum of `ascent.npz` in this
  folder is `abbe700c17d2d775d140dbcf25d911eab3b5ac9270cddcb4572c7fb4506666aa`.
- **Processing:** the pickled array in `ascent.dat` was loaded once from the
  checksum-verified file and saved unchanged in NumPy's compressed `.npz`
  format, so that no pickle is needed to read it. The script that produced it
  (`scripts/fetch_data.py`) is part of the lecture-notes repository,
  <https://github.com/aalsammani/numerical-linear-algebra>.
- **Reading it:** `numpy.load("data/ascent.npz")["image"]`.
