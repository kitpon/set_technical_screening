# Finansia HERO Dashboard — Online Bundle

This directory is ready to publish as a static website, including GitHub Pages.

## Contents

- `index.html`: lightweight entry page
- `dashboard_data.json`: scanner, TD, Minervini, and VCP data
- `chart_data/*.json`: chart histories loaded only when requested
- `.nojekyll`: prevents GitHub Pages from applying Jekyll processing

## Local preview

Run an HTTP server from this directory (opening `index.html` through `file://` is
not supported because the online version uses `fetch`):

```powershell
python.exe -m http.server 8000
```

Then open `http://localhost:8000/`.

## Rebuild

From the parent project directory:

```powershell
python.exe signal_engine.py
python.exe build_dashboard.py
python.exe build_online_dashboard.py
```

Commit and publish the contents of this directory. The offline self-contained
`dashboard.html` in the parent directory remains unchanged.
