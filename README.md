# tests-shipout

Tests for \shipout behavior of pLaTeX
based on LaTeX2e 2020-10-01 (dev).
This repository contains some test input (.tex)
and the expected results (.dvi, .pdf)
which should be visually compared with the actual output.

All files are licensed under MIT License.

## How to test

The new implementation is written in platex.cfg,
which is read at the start of pLaTeX (in `\everyjob`).

1. Obtain `pLaTeX2e <2020-10-01>-pre-1` or later
   (at least texjporg/platex@8b8aca4).
2. Build the platex-dev format.
   `pLaTeX2e <2020-10-01>-pre-1 (based on LaTeX2e <2020-10-01> pre-release-9)`
3. Run `make` in top directory.  Confirm the followings:
   * You don't get any low-level engine errors.
   * You don't see any visual difference between `foo.pdf` and `foo-test.pdf`.

## Known issues

* `atbegshi_nextpage_tate.tex`:
  Some incompatibility; no visual check.
  Confirm that it does not cause any low-level engine errors.
* `everyshi_tikz_2.tex`:
  Shading etc. is not working, but it's not our fault.
  See pgf-tikz/pgf#900.

----
Japanese TeX Development Community
