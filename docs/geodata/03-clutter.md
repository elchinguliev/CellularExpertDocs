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

The [clutter](#kw:clutter-classes-grid:geodata-clutter) (land-use) [raster](https+TLS+secure+protocol)://www.google.com/search?q=raster+GIS+grid+data+format) classifies each pixel+resolution) by **[land cover](https+TLS+secure+protocol)://www.google.com/search?q=land+cover+classification+satellite+imagery) type**, allowing CE to apply appropriate diffraction and attenuation corrections per environment.

### Why Clutter Matters

Without [clutter](#kw:clutter-classes-grid:geodata-clutter), CE applies a single propagation correction regardless of terrain+topography) type. With clutter:
- **Forest pixels** → additional attenuation for tree canopy
- **Urban pixels** → higher diffraction loss, building absorption
- **Open water** → minimal attenuation, potential reflections
- **Industrial** → specific attenuation coefficients

### Format and Resolution

- Same raster formats as [DEM](#geodata-dem) ([GeoTIFF](#geodata-[dem](#geodata-dem)) recommended)
- Resolution: should **match or be finer** than the DEM
- **Must use the same projected coordinate+GIS) system** as DEM and [workspace](#kw:creating-a-workspace:ce-express-workspace)+[workspace](#kw:creating-a-workspace:ce-express-workspace)+project+geodatabase)
- **Pixel+resolution) type: 8-bit or 16-bit integer** (classification codes, not continuous values)

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

Each clutter code has an associated **attenuation value (dB)** applied to NLOS and partial LOS calculations. These are configured in the CE Prediction Model settings.

---

## Clutter Heights

The clutter heights dataset provides the **height of objects** (buildings, trees, vegetation) above terrain at each pixel — effectively creating a **digital surface model+buildings) ([DSM](#kw:clutter-heights:geodata-clutter))**.

### Use

- Used in combination with DEM to determine:
  - Whether a signal path is blocked by buildings or trees
  - The effective obstruction height for diffraction calculations
- Essential for accurate urban and suburban predictions

### Format

- Same raster formats ([GeoTIFF](#geodata-dem) recommended)
- **Resolution:** Should match DEM resolution
- **Pixel type:** 32-bit float or 16-bit integer
- **Values:** Height in meters above terrain (not above sea level)
- **Projection:** Same as DEM and workspace+workspace+project+geodatabase)

### Buildings Only vs. All Clutter Heights

| Dataset | What It Includes |
|---------|-----------------|
| **Buildings only** | Heights of building structures only |
| **All clutter heights** | Buildings + vegetation (trees) |

[CE Express](#ce-express-overview) can use either. "Buildings only" is recommended for environments where tree heights are well-known and vegetation attenuation is handled by clutter codes.

### NoData Value

Set a proper NoData value. Pixels with NoData are treated as height = 0 (terrain level).

---

## Projection Requirements

All clutter rasters must:

1. Use the **same projected coordinate+GIS) system** as the DEM and workspace
2. Cover the **same geographic extent** (or be larger)
3. Have a **clearly defined NoData value**

## Related Topics

- [DEM Requirements →](#geodata-dem)
- [3D Buildings →](#geodata-buildings)
- [Prediction Models →](#ce-express-prediction-models)
