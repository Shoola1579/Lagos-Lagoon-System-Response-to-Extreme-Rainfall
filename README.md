# Lagos Lagoon System Response to Extreme Rainfall

Hydrological modelling case study: **Lagos Island, Lagos State, Nigeria**

**Live app:** https://YOUR-USERNAME.github.io/Lagos-Lagoon-System-Response-to-Extreme-Rainfall/

A browser-based tool that estimates how the Lagos lagoon system responds to rainfall, from everyday weather to extreme storms. It runs entirely in the browser, with no server or installation.

## What the app does

**Daily forecast.** Downloads the latest rainfall forecast (Open-Meteo) for Lagos Island and four points across the lagoon basin, and models the next week automatically. For each day it reports runoff, peak inflow, lagoon water level, a street-flooding index, the chance that the lagoon passes its critical level, a risk class, and a plain-language reading with suggested actions. Ranges come from 80 simulations that vary the forecast rain, curve number, surge and outlet capacity.

**Scenario explorer.** Choose a storm (rainfall depth and duration) and see the inflow hydrograph, lagoon water level, flood duration and a written interpretation. Presets include storms from the 1981-2025 daily rainfall record and the original Aim 3 storms.

**Climate record.** Rainfall trend, seasonal cycle, how often months are very wet, monthly and daily return periods, and satellite sea-level trend and seasonality.

## How it works

- SCS Curve Number runoff (CN 76.54, adjusted for antecedent moisture from the previous 5 days of rain).
- A gamma-type unit hydrograph for the 4,500 km2 basin (18 h time lag).
- A 15-minute lagoon water balance with tide, surge, outlet flow, evaporation and direct rain.
- A street-drainage index for the paved island (assumed runoff coefficient 0.75, drainage capacity 15 mm/h).

## Data used

| Data | Source file | Use |
|---|---|---|
| Monthly rainfall, evaporation, streamflow | MET_DATA.csv | Climate record, monthly evaporation |
| Daily rainfall 1981-2025 | Lagos_Lagoon_Daily_Rainfall.csv | Daily return periods, storm presets |
| Satellite sea level 1993-2025 | Lagos_Sea_Level_Daily.csv | Sea-level trend and seasonality |
| Aim 1 frequency analysis | AIM1_return_periods.csv | Monthly design depths |
| Lagos Island boundary | lagos_island.shp | Study-area map |
| Live rainfall and sea level | Open-Meteo | Daily forecast |

## Limitations

- Parameters were calibrated to literature peak flows and water levels (6 and 3 reference points), not to a continuous gauge record. Use results for scenario screening and planning, not operational forecasting.
- The Aim 3 storm depths (120 to 425 mm) are about 1.7 to 2.7 times the values in the 1981-2025 daily record. The daily data is gridded and cannot show short bursts, but these depths need a source.
- The 237.79 km2 storage area is the Lagos Island Local Government Area boundary, which includes lagoon water, not a measured lagoon area.
- The streamflow column in MET_DATA.csv was derived from water level; its units and rating curve are unconfirmed and it is used only as a rough indicator.
- Sea-level data are daily means, so tides and short local surges are not represented. They do not support the 2.0 m rain-linked surge used in Aim 3.
- The street-flooding index and the forecast uncertainty ranges are model assumptions, not calibrated values.
- Water levels are not validated against measured lagoon records, and there is no elevation data, so the app does not map flood depth or extent.

## Updating the app

Edit or replace `index.html` in this repository and commit. GitHub Pages republishes within a minute or two. Press Ctrl+F5 to see the newest version.

## Author

YOUR NAME, YOUR INSTITUTION, YEAR
