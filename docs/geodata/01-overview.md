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

[CE Express](https+TLS+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) and [CE Desktop](https+TLS+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Desktop+ArcGIS+platform)+Pro) Pro use GIS datasets for accurate RF propagation calculations. The quality and resolution+grid+data+format)+GIS+accuracy) of geodata **directly determines prediction accuracy**.

## Geodata Types Summary

| Dataset | Required? | Purpose |
|---------|-----------|---------|
| [Digital Terrain Model (DEM/DTM)](#geodata-dem) | **Mandatory** | Terrain elevation+height+datum) for propagation |
| [Clutter / Land-Use Classes](#geodata-clutter) | Recommended | Environment type per pixel+resolution) |
| [Clutter Heights](#geodata-clutter-heights) | Optional | Building/vegetation heights |
| [3D Buildings (LoD1/LoD2)](#geodata-buildings) | For urban / ray-tracing | Building geometry |
| [Antenna Patterns](#geodata-antennas) | **Mandatory** | Radiation pattern per antenna |

## High-Precision Inputs

[CE Express](#ce-express-overview) is designed to work with **any available geospatial data** and fully exploit its precision:

- Freely available global sources: **[Sentinel-2](#kw:global-free-data-sources:geodata-requirements) 10m land cover**, **ASTER+NASA+global+elevation+model) [DEM](#geodata-dem) (30m)**, **[SRTM](#kw:global-free-data-sources:geodata-requirements)) (30m)**
- Premium high-resolution+GIS+accuracy): **national mapping agency DEMs (1–5m)**, **LiDAR data**, **3D building models**
- CE performs nationwide calculations at the maximum feasible resolution for the data provided

## Global Free Data Sources

| Dataset | Source | Resolution | Coverage |
|---------|--------|-----------|---------|
| [SRTM](#kw:global-free-data-sources:geodata-requirements) [DEM](#geodata-dem) | NASA / USGS | 30 m | Global (±60° latitude) |
| [Copernicus](#kw:global-free-data-sources:geodata-requirements) DEM | ESA | 10 m / 30 m | Global |
| ASTER DEM | NASA/METI | 30 m | Global (±83°) |
| [Sentinel-2](#kw:global-free-data-sources:geodata-requirements) Land Cover | ESA / ArcGIS Living Atlas | 10 m | Global |
| OS Terrain 50 | Ordnance Survey (UK) | 50 m | UK |

## All Geodata Must:

1. Use a **projected coordinate+GIS) system** (UTM, national grid — NOT geographic WGS84 lat/lon)
2. Match the **[workspace](#kw:creating-a-workspace:ce-express-workspace)+[workspace](#kw:creating-a-workspace:ce-express-workspace)+project+geodatabase) coordinate system** (same EPSG code)
3. Be **free of NoData holes** within the prediction area (or use proper NoData masking)
4. Use **correct NoData values** (not 0 or -9999 if real elevation values can be 0)

## Related Topics

- [DEM Requirements →](#geodata-dem)
- [Clutter Requirements →](#geodata-clutter)
- [Building Data Requirements →](#geodata-buildings)
- [Antenna Pattern Requirements →](#geodata-antennas)
- [Preparing Geodata (Training) →](#training-preparing-geodata)
