# Geodata & Rasters

[CE Express]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) uses [raster]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=raster+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+grid+data+format) files to model [terrain](https://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography) and [land use](https://www.google.com/search?q=land+use+land+cover+classification+GIS) when calculating RF predictions. These files must be prepared and placed on the [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) server before running any predictions.

## Required Files

| File | Required | Description |
|---|---|---|
| `elevation.tif` | **Yes** | [Digital [Terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) Model](https://www.google.com/search?q=Digital+Terrain+Model+[DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation+data)+bare+earth) ([DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model)) — ground [elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum) in metres |
| `clutterClasses.tif` | No | [Land use](https://www.google.com/search?q=land+use+land+cover+classification+GIS) classification (urban, suburban, forest, water, etc.) |
| `clutterHeight.tif` | No | Height of [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio) above terrain (buildings, trees) in metres |

## Format Requirements

All [raster](https://www.google.com/search?q=raster+GIS+grid+data+format) files must meet the following specification:

- **Format**: [GeoTIFF](https://www.google.com/search?q=GeoTIFF+raster+geospatial+format) (`.tif`)
- **Coordinate Reference System**: Projected CRS (e.g. [UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator), national grid) — **not** geographic [WGS84](https://www.google.com/search?q=WGS84+geographic+coordinate+system) ([EPSG](https://www.google.com/search?q=EPSG+coordinate+reference+system):4326)
- **[NoData](https://www.google.com/search?q=NoData+raster+value+GIS+missing+data) value**: `-9999`
- **All files in the same CRS** as each other and as the [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase) setting

> ⚠️ If any file uses a different CRS or [NoData](https://www.google.com/search?q=NoData+raster+value+GIS+missing+data) value, predictions will fail or produce incorrect results.

## What is a Projected CRS?

A **Projected CRS** represents the Earth's curved surface on a flat plane (in metres). Examples:

| CRS | [EPSG](https://www.google.com/search?q=EPSG+coordinate+reference+system+code+database) Code | Used In |
|---|---|---|
| WGS 84 / [UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator+projection) Zone 34N | [EPSG](https://www.google.com/search?q=EPSG+coordinate+reference+system+code+database):32634 | Lithuania, much of Eastern Europe |
| WGS 84 / [UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator+projection) Zone 35N | EPSG:32635 | Eastern Lithuania, Latvia |
| LKS94 / Lithuania TM | EPSG:3346 | Lithuania national grid |
| [ETRS89](https://www.google.com/search?q=ETRS89+European+coordinate+system) / TM35FIN | EPSG:3067 | Finland |

Use [GIS](https://www.google.com/search?q=GIS+Geographic+Information+System) software (QGIS, [ArcGIS Pro](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+Pro+Esri+desktop+software)) to check or reproject your rasters if needed.

## Preparing Rasters with QGIS (Free)

### Check CRS

1. Open your `.tif` file in QGIS.
2. Right-click the layer → **Properties** → **Information** tab.
3. Look for "CRS" — it should show a Projected CRS, not [EPSG:4326](https://www.google.com/search?q=EPSG+4326+[WGS84](https://www.google.com/search?q=WGS84+World+Geodetic+System+coordinate)+geographic+coordinate+system).

### Reproject to Projected CRS

1. **Raster** menu → **Projections** → **Warp (Reproject)**.
2. Set Target CRS to your required projected CRS.
3. Set NoData value to `-9999`.
4. Save output as `.tif`.

### Check and Set NoData Value

1. **Raster** → **Miscellaneous** → **Build Virtual Raster**, or use the Raster Calculator.
2. Alternatively, use [GDAL](https://www.google.com/search?q=GDAL+geospatial+data+abstraction+library): `gdal_translate -a_nodata -9999 input.tif output.tif`

## Placing Files on the Server

Geodata files must be stored on the **CE Express server** (not the user's computer). Work with your system administrator to:

1. Create a folder for each project (e.g. `D:\geodata\vilnius_2025\`).
2. Copy `elevation.tif` (and optional [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) files) into the folder.
3. Use this server path when creating or configuring a [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase).

## Clutter Classification Values

The `clutterClasses.tif` file assigns a land-use category to each [pixel](https://www.google.com/search?q=pixel+raster+grid+[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+resolution). Typical values:

| Value | Class |
|---|---|
| 0 | Open / Water |
| 1 | Open Rural |
| 2 | Suburban |
| 3 | Urban |
| 4 | Dense Urban |
| 5 | Forest |
| 6 | Industrial |

The exact values and their mapping to propagation loss are configured in the prediction model settings.

## Related Pages

- [Workspaces](workspace.md) — linking geodata to a workspace
- [RF Prediction](rf-prediction.md) — how geodata is used in predictions
- [System Requirements](../installation/requirements.md) — server storage recommendations
