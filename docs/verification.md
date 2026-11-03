# Verification — 04/11/2026

This repository is a static interface exercise. The audit reads the actual inline
JavaScript and markup; it does not treat the UI as a working video service.

The inline script generates fictional cards, random years, cast initials
and fixed watching progress. Search only expands an input, profile tabs only change
the active class, and the player button only changes its opacity temporarily.

The audit replaces the static/random IMDb score labels with explicit demonstration
labels. There is no rating-data source or measured viewing history in this project.

No test runner, CI workflow, backend or package manifest is present. The inline
script was syntax-checked with Node.js `vm.Script`. Chromium loaded the real HTML
from a local HTTP server at 1440×1000 and 390×844. Both viewports rendered 10 cards
in the first row, expanded/collapsed search, changed a profile tab, and had no
horizontal overflow or JavaScript page errors. Screenshots in `docs/screenshots/`
come from this browser run and were visually inspected.

Two external Unsplash photo IDs (`1518929458113-24d9791185ba` and
`1608889175638-9322300c46e3`) failed with `ERR_BLOCKED_BY_ORB` on both viewports.
The hero background can therefore be missing. They were not replaced with assets
whose rights were unknown. External-asset reliability and a complete media-license
register remain open; these screenshots do not establish a production-ready site.

External images/fonts remain dependent on their providers. Their presence in the
HTML is provenance information, not evidence that each asset's license was checked.
