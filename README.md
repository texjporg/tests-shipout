# tests-shipout

Tests for \shipout behavior of pLaTeX
based on LaTeX2e 2020-10-01 (dev).
This repository contains some test input (.tex)
and the expected results (.dvi, .pdf)
which should be visually compared with the actual output.

All files are licensed under MIT License.

## Known issues

* `atbegshi_nextpage_tate.tex`:
  Some incompatibility; no visual check.
  Confirm that it does not cause any low-level engine errors.
* `everyshi_tikz_2.tex`:
  Shading etc. is not working, but it's not our fault.
  See pgf-tikz/pgf#900.

----
Japanese TeX Development Community
