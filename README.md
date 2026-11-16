# OpenMPController

Provides `omp_set_num_threads()` to set the number of OpenMP threads, for example when linking against a vendor-optimised BLAS/LAPACK library.

Compatibility updates by Renova.

Version 0.2.5.9002: `src/omp_set_num_threads_ptr.c` includes `<omp.h>` (inside the existing `#ifdef _OPENMP` guard) before the R headers, so R's `match` macro from `Rinternals.h` no longer rewrites `#pragma omp ... declare variant match(...)` in newer `omp.h` headers, which stopped the build with the Windows ARM64 (LLVM) toolchain. Function bodies and routine registration are unchanged.

Version 0.2.5.9001: metadata only: an `Authors@R` field is added for the existing single author and maintainer and the stale `Date` field is removed.

## Install

```r
install.packages("OpenMPController", repos = c(
  Renova = "https://renova-r.r-universe.dev",
  CRAN = "https://cloud.r-project.org"
))
```

See the [R-universe package page](https://renova-r.r-universe.dev/OpenMPController) for builds and installation. This release is tagged on GitHub as `renova-0.2.5.9002`:

```r
remotes::install_github("renova-r/OpenMPController@renova-0.2.5.9002")
```

[Release notes](NEWS.md) · [Renova package directory](https://github.com/renova-r/revival-catalog)

OpenMPController is by Simon Guest; the original CRAN package is at <https://CRAN.R-project.org/package=OpenMPController>. License: GPL-2; see [COPYING](COPYING). The original README is kept as [README.upstream.md](README.upstream.md).
