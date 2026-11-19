# Technical validation of version 1.0

Validation date: 19 November 2026. Scope: manuscript v12 and its figures.

## Data and calculations

All seven existing automated tests passed. They cover document integrity, historical thematic family assignments, figure dimensions and key labels, word-form frequencies against the archived reference, mathematical edge cases, stability of portal directions and flow conservation in the selection pathways.

`scripts/reproduce.py` recalculated 84 word-form comparisons (fourteen forms × three selection variants × two text versions), together with Chinese and BookTok family counts. The outputs match the verified data in content. The underlying data were not changed. Each text version covers 49 unique German articles; removing the English model-generated story reduces the token count by 1,217.

The case index contains 24 unique IDs: 21 main contributions, two additional comments and one additional journalistic report. The 21 main IDs match the cases used in the accepted and finally edited manuscript v12.

## Figures and files

Both figures were regenerated from the included sources in the publication directory. Their PNGs match the verified v12 figures pixel for pixel: Figure 1 measures 1,890 × 2,804 pixels and Figure 2 measures 1,890 × 2,520 pixels. The print files are 120 mm wide and 178 mm and 160 mm high, respectively. English descriptions accompany the original German figures and reading texts.

Relative Markdown links were checked for existing file targets. Text files were checked for local user paths and common credential and private-key patterns; no matches were found. This is a targeted file check, not a comprehensive rights or secrets audit. Checksums for all published files appear in `SHA256SUMS.json`; each figure folder also has its own manifest.

## Environment and scope

The checks used Python 3.12.14, ReportLab 4.4.9, Pillow 13.0.0, pypdf 6.21.4 and Poppler/pdftoppm. Python package versions are recorded in `requirements.txt`. Validation was performed locally with the existing environment in a fresh copy of the GitHub repository, rather than in a newly installed environment or on GitHub Actions.

The checks establish computational, flow and file consistency. They do not replace independent coding or linguistic verification. Original-text extraction and tokenisation require the private source archive; the additional metadata stress test is documented only as an aggregate result. Source checking and further limits are explained in [Data collection and verification](docs/Erhebung_und_Pruefung.md) and [Data and limitations](docs/Daten_und_Grenzen.md).
