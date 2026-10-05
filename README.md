# Oceanographic forcing for the Cox's Bazar–Teknaf coast (1993–2023)

One notebook, `ocean_forcing.ipynb`, that gathers simple oceanographic context for a shoreline-change report:
surface currents, sea surface temperature (HYCOM via Google Earth Engine), significant wave height and direction
(ERA5 via the free Open-Meteo Marine API) and cyclones (IBTrACS), with an exploratory comparison against six
erosion/accretion hotspot zones.

## How to run it (Google Colab)

1. In Colab choose **File > Open notebook > GitHub**, paste this repository's address and open `ocean_forcing.ipynb`.
2. Edit `GEE_PROJECT = "your-gee-project-id"` in the CONFIG cell (the only cell you need to edit).
3. Choose **Runtime > Run all** and approve the Earth Engine sign-in when asked.
   The wave download takes several minutes (it respects the free-tier rate limits).

## Outputs

Everything is written to `/content/ocean_outputs` and zipped to `ocean_outputs.zip`, which downloads at the end:

- **Figures (300 dpi PNG):** `Fig_currents_seasonal`, `Fig_SST_seasonal`, `Fig_SST_trend`,
  `Fig_waves_climatology_trend`, `Fig_waves_seasonal`, `Fig_hotspot_forcing`, `Fig_cyclones`.
- **Tables (CSV):** `hycom_*`, `sst_annual`, `era5_wave_stats`, `hs_monthly`, `hs_annual`, `hotspot_forcing`,
  `hotspot_correlations`, `cyclones_250km`.
- **`SUMMARY.json`**, also printed under `==== SUMMARY (send to Claude) ====`.

Send the zip and the printed SUMMARY back to Claude.
