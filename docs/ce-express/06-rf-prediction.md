---
id: ce-express-rf-prediction
title: RF Prediction
product: CE Express
version: "7.3"
category: Calculations
order: 6
related:
  - ce-express-quick-rf
  - ce-express-prediction-models
  - ce-express-geodata-sets
  - geodata-requirements
  - ce-express-prediction-history
---

# RF Prediction

[RF Prediction]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=RF+radio+frequency+prediction+coverage+planning) calculates **map-based [raster]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=raster+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+grid+data+format) outputs** representing expected signal or radio performance across a coverage area.

## What RF Prediction Uses

Predictions are influenced by:
- **[Network objects](https://www.google.com/search?q=radio+network+objects+sites+cells+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System))** — cells, sites, antennas ([azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north), tilt, height, power, frequency, technology)
- **Configuration parameters** — [bandwidth](https://www.google.com/search?q=channel+bandwidth+radio+frequency+[MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit)), [MIMO](https://www.google.com/search?q=MIMO+Multiple+Input+Multiple+Output+antenna), duplex mode, losses
- **Geodata** — [terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) [elevation](https://www.google.com/search?q=elevation+model+[terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography)+height+datum) ([DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain)), [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning)/[land use](https://www.google.com/search?q=land+use+land+cover+classification+GIS), buildings
- **Equipment definitions** — antenna patterns, [propagation models](https://www.google.com/search?q=radio+propagation+models+comparison+telecom), calculation templates

## Prediction Types

| Output Type | Description |
|-------------|-------------|
| Coverage (signal level) | Received signal strength in [dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit) |
| [Path Loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit)) | Signal [attenuation](https://www.google.com/search?q=signal+attenuation+loss+radio+propagation) in [dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit) |
| [Best Server](https://www.google.com/search?q=best+server+analysis+coverage+planning+RF) | Which [cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) provides the best signal at each point |
| [Interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent) | [Interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent) level across the area |
| [RSRP](https://www.google.com/search?q=RSRP+Reference+Signal+Received+Power+LTE+4G) | Reference Signal Received Power ([4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)/[5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network)) |
| [RSRQ](https://www.google.com/search?q=RSRQ+Reference+Signal+Received+Quality+LTE+4G) | Reference Signal Received Quality ([4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)/[5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network)) |
| [SINR](https://www.google.com/search?q=SINR+Signal+to+Interference+Noise+Ratio) | Signal-to-Interference-plus-Noise Ratio |
| [DL Throughput](https://www.google.com/search?q=downlink+throughput+LTE+4G+calculation) | Downlink data rate estimate ([Mb/s](https://www.google.com/search?q=Mb+s+megabits+per+second+throughput)) |
| Visibility | Radio visibility ([LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation)/[NLOS](https://www.google.com/search?q=NLOS+Non+Line+of+Sight+radio+propagation)) |

## Quick RF Prediction vs Full RF Prediction

| Feature | Quick RF | Full RF |
|---------|----------|---------|
| Speed | Instant | Standard |
| DB impact | **Does not write** to database | Saves to prediction history |
| Use case | What-if testing, parameter comparison | Final results, reporting, documentation |
| Object selection | Uses current object values | Uses saved database values |
| Batch processing | Single [cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)/group | Multiple networks |

→ See [Quick RF Prediction](#ce-express-quick-rf) for rapid testing.

## Running a Full RF Prediction

### Step 1: Select Cells

Select one or more cells using the [Features tool](#ce-express-features) or via a [Network](#ce-express-networks).

### Step 2: Open Prediction Tool

Click **[RF Prediction](https://www.google.com/search?q=RF+radio+frequency+prediction+coverage+planning)** in the left toolbar.

### Step 3: Configure Parameters

**Prediction type:** Choose output (Coverage, [Best Server](https://www.google.com/search?q=best+server+analysis+coverage+planning+RF), [RSRP](https://www.google.com/search?q=RSRP+Reference+Signal+Received+Power+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+4G)), [RSRQ](https://www.google.com/search?q=RSRQ+Reference+Signal+Received+Quality+LTE), [SINR](https://www.google.com/search?q=SINR+Signal+Interference+Noise+Ratio), [Throughput](https://www.google.com/search?q=network+throughput+downlink+uplink+[capacity](https://www.google.com/search?q=network+capacity+planning+telecom)), Interference, etc.)

**[Resolution](https://www.google.com/search?q=spatial+resolution+[raster](https://www.google.com/search?q=raster+GIS+grid+data+format)+GIS+accuracy):** Controls calculation detail and speed:
| [Resolution](https://www.google.com/search?q=spatial+resolution+raster+GIS+accuracy) | Coverage Quality | Speed |
|-----------|-----------------|-------|
| 10 m | Highest | Slowest |
| 25 m | High | Moderate |
| 50 m | Medium | Fast |
| 100 m | Low | Fastest |

> Start with 50–100m for initial planning; use 10–25m for final detailed analysis.

**Radius:** Maximum prediction radius from each [site](https://www.google.com/search?q=cell+site+tower+base+station+location) (meters).

**[Propagation model](https://www.google.com/search?q=radio+wave+propagation+model+telecom):** Select the model appropriate for your environment.
→ See [Prediction Models](#ce-express-prediction-models)

**Receiver height:** Height of the mobile receiver above ground (typically 1.5m for outdoor; custom for indoor, vehicle, rooftop).

### Step 4: Run

Click **Run** — a progress indicator appears. Results render as raster layers in the map when complete.

## Required Inputs

| Input | Required? | Notes |
|-------|-----------|-------|
| [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain) (terrain) | **Mandatory** | Must cover the full prediction area with correct [projection](https://www.google.com/search?q=map+projection+coordinate+system+GIS) |
| [Clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning)/[land use](https://www.google.com/search?q=land+use+land+cover+classification+GIS) | Recommended | Significantly improves accuracy in mixed environments |
| 3D buildings | For urban micro / ray-tracing | Required for [COST-231](https://www.google.com/search?q=COST-231+propagation+model+telecom) W-I and ray-tracing models |
| [Antenna pattern](https://www.google.com/search?q=antenna+radiation+pattern+file+format+MSI) | **Mandatory** | Each cell must have an antenna assigned (.msi or .pln) |
| [Propagation model](https://www.google.com/search?q=radio+wave+propagation+model+telecom) | **Mandatory** | Configured in [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase) or per-cell |

> If [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster) does not cover the prediction area, the prediction will produce empty results. Check geodata coverage in [Geodata Sets](#ce-express-geodata-sets).

## Prediction Results

Results appear as raster layers in the map. From the [Prediction History](#ce-express-prediction-history) panel:
- Toggle layers on/off
- Customize colour scales and thresholds
- Compare multiple predictions
- [Export](https://www.google.com/search?q=data+export+GIS+raster+vector) results as **[GeoTIFF](https://www.google.com/search?q=GeoTIFF+raster+geospatial+format)** raster

## Common Issues

| Problem | Cause | Fix |
|---------|-------|-----|
| Empty/blank result | [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster) not loaded or wrong [projection](https://www.google.com/search?q=map+projection+coordinate+system+GIS) | Check geodata set coverage and projection |
| No result layer | Antenna not assigned to cell | Assign [antenna pattern](https://www.google.com/search?q=antenna+radiation+pattern+file+format) in cell properties |
| Very slow prediction | Fine resolution over large area | Increase resolution to 50–100m; reduce radius |
| Out of memory | Large area at fine resolution | Split area, reduce radius, use coarser resolution |
| License error | Prediction module not licensed | Check License Manager — contact support |

→ See [Troubleshooting RF Prediction](#troubleshooting-rf-prediction)

## Related Topics

- [Quick RF Prediction →](#ce-express-quick-rf)
- [Prediction Models →](#ce-express-prediction-models)
- [Geodata Requirements →](#geodata-requirements)
- [Geodata Sets →](#ce-express-geodata-sets)
- [Prediction History →](#ce-express-prediction-history)
- [Networks (Batch Prediction) →](#ce-express-networks)
