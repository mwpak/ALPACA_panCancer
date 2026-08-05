# ALPACA

ALPACA (A Location-wise Proteome/transcriptome Abundance Comparative Analyzer)
is a browser-based visual data-mining tool for comparing cancer transcriptomic
and proteomic abundance by subcellular location and biological pathway.

The public site is a static export of the original Django frontend. It does not
require Django, a database, or an API server.

## Repository layout

- `docs/` contains the complete GitHub Pages site.
- `frontend/src/` contains the React/D3 source.
- `frontend/webpack.config.js` builds the JavaScript bundle directly into
  `docs/static/frontend/`.
- `docs/static/data/` contains the datasets loaded by the browser.

## Build the frontend

```sh
cd frontend
npm ci
npm run build
```

Serve `docs/` over HTTP when testing; browser data requests will not work
reliably from a `file://` URL.
