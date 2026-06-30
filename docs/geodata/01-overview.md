---
id: geodata-requirements
title: Geodata Requirements
product: Both
category: Geodata
order: 1
related:
  - ce-express-geodata-sets
  - ce-express-workspace
  - ce-express-rf-prediction
  - geodata-dem
  - geodata-clutter
  - geodata-buildings
---

# Geodata Requirements for CE Software

CE Express and CE Desktop Pro use GIS datasets for accurate RF propagation calculations. The quality and resolution of geodata **directly determines prediction accuracy**.

## Geodata Types Summary

| Dataset | Required? | Purpose |
|---------|-----------|---------|
| Digital Terrain Model (DEM/DTM) | **Mandatory** | Terrain elevation for propagation |
| [Clutter](#kw:clutter-classification-values:ce-express-geodata) / Land-Use Classes | Recommended | Environment type per pixel |
| [Clutter](#kw:clutter-classification-values:ce-express-geodata) Heights | Optional | Building/vegetation heights |
| 3D Buildings (LoD1/LoD2) | For urban / ray-tracing | Building geometry |
| [Antenna Patterns](#kw:importing-antenna-patterns:ce-express-antenna) | **Mandatory** | Radiation pattern per antenna |

## High-Precision Inputs

CE Express is designed to work with **any available geospatial data** and fully exploit its precision:

- Freely available global sources: **[Sentinel-2](#kw:global-free-data-sources:none) 10m land cover**, **ASTER DEM (30m)**, **[SRTM](#kw:global-free-data-sources:none) (30m)**
- Premium high-resolution: **national mapping agency DEMs (1–5m)**, **LiDAR data**, **3D building models**
- CE performs nationwide calculations at the maximum feasible resolution for the data provided

## Global Free Data Sources

| Dataset | Source | Resolution | Coverage |
|---------|--------|-----------|---------|
| [SRTM](#kw:global-free-data-sources:none) DEM | NASA / USGS | 30 m | Global (±60° latitude) |
| [Copernicus](#kw:global-free-data-sources:none) DEM | ESA | 10 m / 30 m | Global |
| ASTER DEM | NASA/METI | 30 m | Global (±83°) |
| [Sentinel-2](#kw:global-free-data-sources:none) Land Cover | ESA / ArcGIS Living Atlas | 10 m | Global |
| OS Terrain 50 | Ordnance Survey (UK) | 50 m | UK |

## All Geodata Must:

1. Use a **projected coordinate system** (UTM, national grid — NOT geographic WGS84 lat/lon)
2. Match the **workspace coordinate system** (same EPSG code)
3. Be **free of NoData holes** within the prediction area (or use proper NoData masking)
4. Use **correct NoData values** (not 0 or -9999 if real elevation values can be 0)

## Related Topics

- DEM Requirements →
- Clutter Requirements →
- Building Data Requirements →
- [Antenna Pattern](#kw:managing-the-antenna-library:ce-express-antenna) Requirements →
- Preparing Geodata (Training) →
