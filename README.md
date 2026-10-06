# Lagos Lagoon System Response to Extreme Rainfall

Live web app for the project *Hydrological modelling of the Lagos lagoon system's response to extreme rainfall events: a case study of Lagos Island, Lagos State, Nigeria*.

Enter rainfall depth and duration (plus optional curve number, surge, outlet capacity and tide) and the app predicts runoff depth, peak discharge, lagoon water level, flood and overflow duration, risk class and approximate return period. It is a JavaScript port of the v3 model: SCS-CN runoff, a gamma-type hydrograph, and a 15-minute lagoon water balance with tide, surge, outlet flow and evaporation.

## Deploy on GitHub Pages

1. Create a new GitHub repository, for example `lagos-flood-predictor`.
2. Upload `index.html` and `README.md` to the repository root.
3. Go to Settings > Pages. Under Build and deployment choose Deploy from a branch, select `main` and `/ (root)`, then Save.
4. After about a minute the app is live at `https://<your-username>.github.io/lagos-flood-predictor/`.

## Limits

Parameters were calibrated against literature peak flows and water levels, not a continuous gauge record. Use results for scenario screening and planning, not operational forecasting.
