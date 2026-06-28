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

[CE Express]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) and [CE Desktop]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Desktop+[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+Pro) Pro use [GIS](https://www.google.com/search?q=GIS+Geographic+Information+System) datasets for accurate RF propagation calculations. The quality and [resolution](https://www.google.com/search?q=spatial+resolution+[raster](https://www.google.com/search?q=raster+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+grid+data+format)+GIS+accuracy) of geodata **directly determines prediction accuracy**.

## Geodata Types Summary

| Dataset | Required? | Purpose |
|---------|-----------|---------|
| [Digital Terrain Model (DEM/DTM)](#geodata-dem) | **Mandatory** | [Terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) [elevation](https://www.google.com/search?q=elevation+model+[terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography)+height+datum) for propagation |
| [Clutter / Land-Use Classes](#geodata-clutter) | Recommended | Environment type per [pixel](https://www.google.com/search?q=pixel+raster+grid+[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+resolution) |
| [Clutter Heights](#geodata-clutter-heights) | Optional | Building/vegetation heights |
| [3D Buildings (LoD1/LoD2)](#geodata-buildings) | For urban / ray-tracing | Building geometry |
| [Antenna Patterns](#geodata-antennas) | **Mandatory** | [Radiation pattern](https://www.google.com/search?q=antenna+radiation+pattern+horizontal+vertical) per antenna |

## High-Precision Inputs

[CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) is designed to work with **any available geospatial data** and fully exploit its precision:

- Freely available global sources: **[Sentinel-2](https://www.google.com/search?q=Sentinel+2+ESA+satellite+multispectral+imagery) 10m [land cover](https://www.google.com/search?q=land+cover+classification+satellite+imagery)**, **[ASTER](https://www.google.com/search?q=ASTER+[DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster)+NASA+global+elevation+model) [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain) (30m)**, **[SRTM](https://www.google.com/search?q=SRTM+Shuttle+Radar+Topography+Mission+[DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster)) (30m)**
- Premium high-[resolution](https://www.google.com/search?q=spatial+resolution+[raster](https://www.google.com/search?q=raster+GIS+grid+data+format)+GIS+accuracy): **national mapping agency DEMs (1–5m)**, **[LiDAR](https://www.google.com/search?q=LiDAR+Light+Detection+Ranging+point+cloud) data**, **[3D building](https://www.google.com/search?q=3D+building+model+urban+GIS) models**
- CE performs nationwide calculations at the maximum feasible resolution for the data provided

## Global Free Data Sources

| Dataset | Source | Resolution | Coverage |
|---------|--------|-----------|---------|
| [SRTM](https://www.google.com/search?q=SRTM+Shuttle+Radar+Topography+Mission) DEM | NASA / USGS | 30 m | Global (±60° latitude) |
| [Copernicus](https://www.google.com/search?q=Copernicus+DEM+ESA+elevation+model) DEM | ESA | 10 m / 30 m | Global |
| [ASTER](https://www.google.com/search?q=ASTER+DEM+NASA+global+elevation+model) DEM | NASA/METI | 30 m | Global (±83°) |
| [Sentinel-2](https://www.google.com/search?q=Sentinel+2+ESA+satellite+land+cover) [Land Cover](https://www.google.com/search?q=land+cover+classification+satellite+imagery) | ESA / [ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform) Living Atlas | 10 m | Global |
| OS Terrain 50 | Ordnance Survey (UK) | 50 m | UK |

## All Geodata Must:

1. Use a **[projected coordinate](https://www.google.com/search?q=projected+coordinate+system+[UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator+projection)+GIS) system** ([UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator), national grid — NOT geographic [WGS84](https://www.google.com/search?q=WGS84+geographic+coordinate+system) lat/lon)
2. Match the **[workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase) [coordinate system](https://www.google.com/search?q=coordinate+reference+system+CRS+GIS)** (same [EPSG](https://www.google.com/search?q=EPSG+coordinate+reference+system) code)
3. Be **free of [NoData](https://www.google.com/search?q=NoData+raster+value+GIS+missing+data) holes** within the prediction area (or use proper [NoData](https://www.google.com/search?q=NoData+raster+value+GIS+missing+data) masking)
4. Use **correct NoData values** (not 0 or -9999 if real [elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum) values can be 0)

## Related Topics

- [DEM Requirements →](#geodata-dem)
- [Clutter Requirements →](#geodata-clutter)
- [Building Data Requirements →](#geodata-buildings)
- [Antenna Pattern Requirements →](#geodata-antennas)
- [Preparing Geodata (Training) →](#training-preparing-geodata)
