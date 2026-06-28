---
id: geodata-dem
title: Digital Terrain Model (DEM/DTM)
product: Both
category: Geodata
order: 2
related:
  - geodata-requirements
  - geodata-clutter
  - ce-express-geodata-sets
---

# Digital Terrain Model (__S2__ / __S3__)

The [Digital [Terrain]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography) Model]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=Digital+[Terrain](https://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography)+Model+[DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation+data)+bare+earth) ([DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster) or [DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation+data)) provides **terrain [elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum) data** used in all RF propagation calculations. It is the **single most important geodata input** in [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform).

## Requirements

### Format

Supported [raster](https://www.google.com/search?q=raster+GIS+grid+data+format) formats:
- **[GeoTIFF](https://www.google.com/search?q=GeoTIFF+[raster](https://www.google.com/search?q=raster+GIS+grid+data+format)+geospatial+format)** (.tif, .tiff) — **recommended**
- [ERDAS](https://www.google.com/search?q=ERDAS+Imagine+raster+GIS+format) Imagine (.img)
- [ASCII Grid](https://www.google.com/search?q=ASCII+Grid+raster+format+GIS) (.asc)
- [ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform) Grid format
- Any [GDAL](https://www.google.com/search?q=GDAL+geospatial+data+abstraction+library)-supported raster format

### Resolution

| Area Type | Minimum [Resolution](https://www.google.com/search?q=spatial+resolution+raster+GIS+accuracy) | Recommended |
|-----------|-------------------|-------------|
| Rural / Open | 30 m | 20 m |
| Suburban | 20 m | 10 m |
| Urban macro | 10 m | 5 m |
| Urban micro / small cells | 5 m | 1–2 m |

> Higher [resolution](https://www.google.com/search?q=spatial+resolution+raster+GIS+accuracy) = more accurate predictions, but slower calculation time and larger file size.

### Coordinate System (Projection)

- **Must use a [projected coordinate](https://www.google.com/search?q=projected+coordinate+system+[UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator+projection)+GIS) system** (e.g., [UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator) Zone XX, [ETRS89](https://www.google.com/search?q=ETRS89+European+coordinate+system)/TM, national grids)
- **Do NOT use geographic coordinates ([WGS84](https://www.google.com/search?q=WGS84+geographic+coordinate+system) [EPSG](https://www.google.com/search?q=EPSG+coordinate+reference+system):4326)**
- Must exactly match the **[workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase) [EPSG](https://www.google.com/search?q=EPSG+coordinate+reference+system+code+database) code**

### Pixel Type

- **32-bit float** (recommended) — supports fractional [elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum) values
- 16-bit integer — acceptable for lower precision needs
- **Do NOT use 8-bit** — insufficient range for elevation values

### NoData Value

- Set a proper [NoData](https://www.google.com/search?q=NoData+raster+value+GIS+missing+data) value (typically -9999 or -32768)
- Do NOT use 0 as [NoData](https://www.google.com/search?q=NoData+raster+value+GIS+missing+data) if the coverage area includes sea level or below-sea-level terrain
- NoData areas within the prediction radius will produce empty results

### Raster Name

- Use descriptive, unique filenames
- Avoid special characters and spaces: use underscores (`terrain_utm35n_2m.tif`)
- The file name becomes the dataset identifier in [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform)

## Vertical Accuracy

| Application | Required Vertical Accuracy |
|-------------|--------------------------|
| Rural macro planning | ≤ 10 m |
| Suburban macro | ≤ 5 m |
| Urban macro | ≤ 2 m |
| Urban micro / indoor | ≤ 1 m |

## Checking Your DEM

Before loading into CE Express, verify:

```bash
# Check projection, resolution, NoData (using GDAL)
gdalinfo your_dem.tif

# Key fields to check:
# - Coordinate System: should be projected (not GEOGCS)
# - Pixel Size: resolution in map units
# - NoData Value: should be set
# - Min/Max: should reflect realistic elevation range
```

## Multi-Resolution Support

CE Express supports **multi-resolution datasets** — you can load different [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster) resolutions for different areas. CE automatically selects the appropriate resolution for each calculation area.

## Related Topics

- [Geodata Overview →](#geodata-requirements)
- [Clutter Classes →](#geodata-clutter)
- [Loading Geodata in CE Express →](#ce-express-geodata-sets)
