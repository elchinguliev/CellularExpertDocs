# Geodata & Rasters

CE Express uses raster files to model terrain and land use when calculating RF predictions. These files must be prepared and placed on the CE Express server before running any predictions.

## Required Files

| File | Required | Description |
|---|---|---|
| `elevation.tif` | **Yes** | Digital Terrain Model (DTM) — ground elevation in metres |
| `clutterClasses.tif` | No | Land use classification (urban, suburban, forest, water, etc.) |
| `clutterHeight.tif` | No | Height of clutter above terrain (buildings, trees) in metres |

## Format Requirements

All raster files must meet the following specification:

- **Format**: GeoTIFF (`.tif`)
- **Coordinate Reference System**: Projected CRS (e.g. UTM, national grid) — **not** geographic WGS84 (EPSG:4326)
- **NoData value**: `-9999`
- **All files in the same CRS** as each other and as the workspace setting

> ⚠️ If any file uses a different CRS or NoData value, predictions will fail or produce incorrect results.

## What is a Projected CRS?

A **Projected CRS** represents the Earth's curved surface on a flat plane (in metres). Examples:

| CRS | EPSG Code | Used In |
|---|---|---|
| WGS 84 / UTM Zone 34N | EPSG:32634 | Lithuania, much of Eastern Europe |
| WGS 84 / UTM Zone 35N | EPSG:32635 | Eastern Lithuania, Latvia |
| LKS94 / Lithuania TM | EPSG:3346 | Lithuania national grid |
| ETRS89 / TM35FIN | EPSG:3067 | Finland |

Use GIS software (QGIS, ArcGIS Pro) to check or reproject your rasters if needed.

## Preparing Rasters with QGIS (Free)

### Check CRS
1. Open your `.tif` file in QGIS.
2. Right-click the layer → **Properties** → **Information** tab.
3. Look for "CRS" — it should show a Projected CRS, not EPSG:4326.

### Reproject to Projected CRS
1. **Raster** menu → **Projections** → **Warp (Reproject)**.
2. Set Target CRS to your required projected CRS.
3. Set NoData value to `-9999`.
4. Save output as `.tif`.

### Check and Set NoData Value
1. **Raster** → **Miscellaneous** → **Build Virtual Raster**, or use the Raster Calculator.
2. Alternatively, use GDAL: `gdal_translate -a_nodata -9999 input.tif output.tif`

## Placing Files on the Server

Geodata files must be stored on the **CE Express server** (not the user's computer). Work with your system administrator to:

1. Create a folder for each project (e.g. `D:\geodata\vilnius_2025\`).
2. Copy `elevation.tif` (and optional clutter files) into the folder.
3. Use this server path when creating or configuring a workspace.

## Clutter Classification Values

The `clutterClasses.tif` file assigns a land-use category to each pixel. Typical values:

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
