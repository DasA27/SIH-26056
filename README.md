# AeroVista Government UI v2.3 — Advanced Statistical Intelligence Prototype

## Run locally

```powershell
npm install
npm run dev
```

Open the Vite URL shown in the terminal (normally `http://localhost:5173`). Keep the terminal running; Vite will hot-reload after file saves.

## What changed in v2.3

- Expanded the demonstration basket from 50 to **200 directional corridors** across 28 hubs.
- Full multi-hub India route network map with modes for **Surge, Route Index, Traffic Weight, Volatility and Confidence**.
- Five route indicators are visible together for the selected corridor.
- User-selectable **side-by-side route comparison**.
- Larger body/detail typography across Backtest, Data Quality, Data Catalogue and analytical panels.
- Explicit chart legends for **AeroVista APIx, DGCA reference and ATF signal**.
- Added lead-time profile, quality trajectory, error profile, elasticity profile and fare-distribution charts.
- Added **AI & Intelligence Lab** with clickable metric explanations.
- Added detailed formula/variable/interpretation/caveat modal for each major metric.
- Added four novelty pillars inspired by the supplied concept: base-fare disaggregation, QC/outlier quarantine, multi-window booking tracking, and Jevons geometric companion.
- Added readable data lineage and schema surfaces.

## Important statistical note

The 200-route weights in this UI are deterministic prototype proxies. They are **not official DGCA weights**. Replace them with the validated official DGCA extraction/aggregation before any real statistical publication.

The Jevons measure and National Airfare Pressure Index are presented as **research/robustness indicators**, not as an automatic replacement for the prescribed core APIx construction.

## Useful public data references for future backend integration

- DGCA-sourced Indian aviation traffic dataset: https://github.com/Vonter/india-aviation-traffic
- Open airport metadata: https://ourairports.com/data/
- India spatial datasets: https://github.com/datameet/maps
