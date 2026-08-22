# Changelog

All notable changes to the Zimbabwe ISP Tracker are recorded here. Format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/); versioning follows
[Semantic Versioning](https://semver.org/) (MAJOR.MINOR.PATCH).

The version number shown here matches the `<meta name="app-version">` tag in `index.html`
and the `v{version}` badge in each page's footer.

## [1.0.0] — 2026-08-22

Baseline versioned release.

### Added
- `lite.html` — no-script fallback page for older phones / slow connections, listing all 10
  POTRAZ-tracked providers with an email- and SMS-based rating option (no backend required).
- Language switching on the Lite page: `lite.html` (English) plus `lite-sn.html` (ChiShona),
  `lite-nd.html` (IsiNdebele), `lite-ny.html` (Chewa), `lite-ts.html` (Shangani/Xitsonga),
  `lite-st.html` (Sotho), `lite-tn.html` (Tswana), `lite-ve.html` (Venda), `lite-xh.html` (Xhosa).
  Draft, machine-assisted translations, flagged as unreviewed on the page itself.
- Cross-browser compatibility banner on `index.html`: feature-detects `fetch`, `Promise`,
  `localStorage`, and CSS grid/flexbox support; points visitors to the Lite page if anything's
  missing, rather than failing silently.
- Version tracking: `<meta name="app-version">` on every page, a footer version badge, and this
  changelog.

### Fixed
- `matokipedo-logo.jpg` was actually HEIC-encoded photo data saved with a `.jpg` extension (an
  iPhone Photos/Preview export quirk) — every browser failed to decode it as the JPEG its
  extension and Content-Type header claimed, showing a broken-image icon everywhere. Re-encoded
  as a genuine JPEG, same filename and dimensions.

### Not yet translated
TjiKalanga, Chibarwe, Khoisan (Tjwao), Nambya, Ndau, and Tonga are not yet available as Lite-page
translations — see `SKILL.md` in the `matokipedo-isp-tracker-qc` skill for why (low confidence in
producing an honest draft rather than a fabricated one for these lower-resourced languages).
They're listed but greyed out in the Lite page's language bar until a real translation exists.

<!--
Template for the next entry — copy this when you ship a change:

## [1.1.0] — YYYY-MM-DD
### Added / Changed / Fixed / Removed
- ...
-->
