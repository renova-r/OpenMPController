# OpenMPController 0.2.5.9002

- `src/omp_set_num_threads_ptr.c`: the `#ifdef _OPENMP` / `#include <omp.h>` / `#endif` block now comes before `#include <R.h>`, `<Rinternals.h>` and `<Rconfig.h>`. `Rinternals.h` defines `match` as `Rf_match`; when `omp.h` was included afterwards, its `#pragma omp begin declare variant match(...)` lines were macro-expanded and the Windows ARM64 (clang, Rtools 4.5) build failed. No function body, signature or native-routine registration changed.
- `DESCRIPTION`: `Version` set to `0.2.5.9002`.

# OpenMPController 0.2.5.9001

Renova release, based on CRAN OpenMPController 0.2-5 (archived on CRAN 2021-09-25).

- `DESCRIPTION`: `Authors@R` added and `Author` rewritten as `Simon Guest [aut, cre]` for the same author and maintainer (metadata only).
- `DESCRIPTION`: stale optional `Date` field removed (metadata only).
- No R, C or documentation files changed.

Release preparation:

- `DESCRIPTION`: `Version` set to `0.2.5.9001`; "Compatibility updates by Renova." appended to `Description`.
- The stale `MD5` file was removed.
- `COPYING` (GNU GPL version 2 text) was added; the `License` field is unchanged.
- `README.md` was rewritten for this release; the original README is kept as `README.upstream.md`. Both are excluded from the R build.
- `NEWS.md` was added and is excluded from the R build.
