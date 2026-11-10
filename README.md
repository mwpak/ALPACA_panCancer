# ALPACA_panCancer

ALPACA_panCancer provides the interactive, precomputed pan-cancer abundance
data analyses for **ALPACA (A Location-wise Proteome/transcriptome Abundance
Comparative Analyzer)**, accompanying the *BMC Medical Genomics* article:

> Minwoo Pak, Dabin Jeong, Sungjoon Park, Jeonghyeon Gu, Sangseon Lee, and
> Sun Kim. **ALPACA: A Visual Data Mining System for Subcellular
> Location-specific Knowledge Mining from Multi-Omics Data in Cancer.**
> *BMC Medical Genomics* **16** (Suppl 1), 336 (2026).
> DOI: [10.1186/s12920-026-02440-4](https://doi.org/10.1186/s12920-026-02440-4)

ALPACA is a browser-based visual data-mining tool for comparing cancer
transcriptomic and proteomic abundance by subcellular location and biological
pathway.

- **Launch ALPACA_panCancer:** https://mwpak.github.io/ALPACA_panCancer/
- **Main ALPACA source code repository:** https://github.com/mwpak/ALPACA

This repository contains the static GitHub Pages deployment and precomputed
pan-cancer datasets. For the ALPACA source code, installation instructions,
and continued development, please visit the main ALPACA repository.

## About this repository

The website is a static export of the original Django frontend. All datasets
and visualization logic run in the browser, so the deployed site does not
require Django, a database, or an API server.

## Repository layout

- `docs/` contains the complete GitHub Pages site.
- `frontend/src/` contains the React/D3 source.
- `frontend/webpack.config.js` builds the JavaScript bundle directly into
  `docs/static/frontend/`.
- `docs/static/data/` contains the datasets loaded by the browser.

## Local preview

Serve `docs/` over HTTP because browser data requests are blocked when
`index.html` is opened directly with a `file://` URL:

```sh
python3 -m http.server 8000 --directory docs
```

Then open http://localhost:8000/.

## Build the frontend

```sh
cd frontend
npm ci
npm run build
```
