---
id: geodata-clutter
title: Clutter Classes and Clutter Heights
product: Both
category: Geodata
order: 3
related:
  - geodata-dem
  - geodata-buildings
  - ce-express-prediction-models
---

# Clutter Classes and Clutter Heights

## Clutter Classes Grid

The [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio) (land-use) [raster]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=raster+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+grid+data+format) classifies each [pixel](https://www.google.com/search?q=pixel+raster+grid+[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+resolution) by **[land cover]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=land+cover+classification+satellite+imagery) type**, allowing CE to apply appropriate [diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation) and [attenuation](https://www.google.com/search?q=signal+attenuation+loss+radio+propagation) corrections per environment.

### Why Clutter Matters

Without [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning), CE applies a single propagation correction regardless of [terrain](https://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography) type. With [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning):
- **Forest pixels** → additional [attenuation](https://www.google.com/search?q=signal+attenuation+loss+radio+propagation) for tree canopy
- **Urban pixels** → higher [diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation) loss, building [absorption](https://www.google.com/search?q=atmospheric+absorption+radio+signal)
- **Open water** → minimal attenuation, potential reflections
- **Industrial** → specific attenuation coefficients

### Format and Resolution

- Same [raster](https://www.google.com/search?q=raster+GIS+grid+data+format) formats as [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain) ([GeoTIFF](https://www.google.com/search?q=GeoTIFF+raster+geospatial+format) recommended)
- [Resolution](https://www.google.com/search?q=spatial+resolution+raster+GIS+accuracy): should **match or be finer** than the [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster)
- **Must use the same [projected coordinate](https://www.google.com/search?q=projected+coordinate+system+[UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator+projection)+GIS) system** as [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster) and [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase)
- **[Pixel](https://www.google.com/search?q=pixel+raster+grid+[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+resolution) type: 8-bit or 16-bit integer** (classification codes, not continuous values)

### Standard Clutter Categories

| Code | Category | Description |
|------|----------|-------------|
| 0 | Open / Rural | Fields, grassland, no significant obstacles |
| 1 | Rural Vegetation | Low vegetation, scattered trees |
| 2 | Forest | Dense tree canopy |
| 3 | Suburban | Low-density residential |
| 4 | Urban | Medium-density mixed use |
| 5 | Dense Urban | High-density city centre |
| 6 | Industrial | Warehouses, factories |
| 7 | Water | Lakes, rivers, sea |
| 8 | Buildings | High-rise or specific building clutter |

> CE allows custom clutter codes — contact Cellular Expert support for mapping assistance.

### Clutter Loss Values

Each clutter code has an associated **attenuation value ([dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit))** applied to [NLOS](https://www.google.com/search?q=NLOS+Non+Line+of+Sight+radio+propagation) and partial [LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation) calculations. These are configured in the CE Prediction Model settings.

---

## Clutter Heights

The clutter heights dataset provides the **height of objects** (buildings, trees, vegetation) above [terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) at each pixel — effectively creating a **[digital surface model](https://www.google.com/search?q=Digital+Surface+Model+[DSM](https://www.google.com/search?q=DSM+Digital+Surface+Model+buildings+trees)+buildings) ([DSM](https://www.google.com/search?q=DSM+Digital+Surface+Model))**.

### Use

- Used in combination with DEM to determine:
  - Whether a signal path is blocked by buildings or trees
  - The effective obstruction height for diffraction calculations
- Essential for accurate urban and suburban predictions

### Format

- Same raster formats ([GeoTIFF](https://www.google.com/search?q=GeoTIFF+raster+geospatial+format) recommended)
- **[Resolution](https://www.google.com/search?q=spatial+resolution+raster+GIS+accuracy):** Should match DEM resolution
- **Pixel type:** 32-bit float or 16-bit integer
- **Values:** Height in meters above terrain (not above sea level)
- **[Projection](https://www.google.com/search?q=map+projection+coordinate+system+GIS):** Same as DEM and [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase)

### Buildings Only vs. All Clutter Heights

| Dataset | What It Includes |
|---------|-----------------|
| **Buildings only** | Heights of building structures only |
| **All clutter heights** | Buildings + vegetation (trees) |

[CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) can use either. "Buildings only" is recommended for environments where tree heights are well-known and vegetation attenuation is handled by clutter codes.

### NoData Value

Set a proper [NoData](https://www.google.com/search?q=NoData+raster+value+GIS+missing+data) value. Pixels with [NoData](https://www.google.com/search?q=NoData+raster+value+GIS+missing+data) are treated as height = 0 (terrain level).

---

## Projection Requirements

All clutter rasters must:

1. Use the **same [projected coordinate](https://www.google.com/search?q=projected+coordinate+system+[UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator+projection)+GIS) system** as the DEM and workspace
2. Cover the **same geographic extent** (or be larger)
3. Have a **clearly defined NoData value**

## Related Topics

- [DEM Requirements →](#geodata-dem)
- [3D Buildings →](#geodata-buildings)
- [Prediction Models →](#ce-express-prediction-models)
