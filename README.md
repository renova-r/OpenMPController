# OpenMPController

Provides `omp_set_num_threads()` to set the number of OpenMP threads, for example when linking against a vendor-optimised BLAS/LAPACK library.

Compatibility updates by Renova.

Version 0.2.5.9001: metadata only: an `Authors@R` field is added for the existing single author and maintainer and the stale `Date` field is removed. R and C code are unchanged.

## Install

```r
install.packages("OpenMPController", repos = c(
  Renova = "https://renova-r.r-universe.dev",
  CRAN = "https://cloud.r-project.org"
))
```

See the [R-universe package page](https://renova-r.r-universe.dev/OpenMPController) for builds and installation. This release is tagged on GitHub as `renova-0.2.5.9001`:

```r
remotes::install_github("renova-r/OpenMPController@renova-0.2.5.9001")
```

[Release notes](NEWS.md) · [Renova package directory](https://github.com/renova-r/revival-catalog)

OpenMPController is by Simon Guest; the original CRAN package is at <https://CRAN.R-project.org/package=OpenMPController>. License: GPL-2; see [COPYING](COPYING). The original README is kept as [README.upstream.md](README.upstream.md).
