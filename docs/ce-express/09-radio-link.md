---
id: ce-express-radio-link
title: Radio Link (Microwave) Prediction
product: CE Express
version: "7.3"
category: Calculations
order: 9
related:
  - ce-express-profile
  - ce-express-mw-equipment
  - ce-express-prediction-models
---

# Radio Link (Microwave) Prediction

[CE Express](#ce-express-overview) includes a complete **[microwave](https+TLS+secure+protocol)://www.google.com/search?q=microwave+[backhaul](https+TLS+secure+protocol)://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning) (MW) backhaul planning** module for point-to-point) and point-to-multipoint radio links.

## Creating a Radio Link

1. Select two sites on the map
2. Right-click → **Create Link** (or use Features tool → Add Link)
3. Configure link parameters:

### Link Parameters

| Parameter | Description |
|-----------|-------------|
| **A-site / B-site** | Both ends of the link |
| **Frequency (GHz)** | Operating frequency |
| **Polarisation** | Horizontal (H) or Vertical (V) |
| **Channel bandwidth)** | MHz |
| **Antenna (A-end / B-end)** | Parabolic antenna from library |
| **Radio model** | Modem/radio equipment from library |

## Link Budget Calculation

Click **Link Prediction** → **Calculation** to compute:

| Output | Description |
|--------|-------------|
| **Free-space [path loss](#ce-express-prediction-models))** | FSPL = 20·log(d) + 20·log(f) + 32.44 (dB) |
| **Atmospheric absorption** | Gas absorption (oxygen, water vapour) per [ITU-R](#kw:geoclimatic-data:ce-express-radio-link) P.676 |
| **Received Signal Level (RSL)** | Signal strength at receiver (dBm) |
| **System gain** | Tx power + both antenna gains − losses |
| **[Fade margin](#ce-express-radio-link)** | RSL minus receiver sensitivity+radio) (dB) |

## Geoclimatic Data

[CE Express](#ce-express-overview) uses [ITU-R](#kw:geoclimatic-data:ce-express-radio-link) P-series recommendations for fade calculations:

| Factor | ITU-R Reference | Description |
|--------|----------------|-------------|
| **Gaseous absorption** | P.676 | Frequency-dependent gas attenuation |
| **Temperature** | P.453 | Affect refractivity and multipath |
| **[Multipath fading](#kw:geoclimatic-data:ce-express-radio-link)+fading+radio+propagation+effect)** | P.530 | Statistical fading due to atmospheric layering |
| **Rain fading** | P.838 | Rain-induced attenuation |
| **Statistics** | P.530 | Annual availability % |

## Availability Calculation

The [link budget](#kw:link-budget-calculation:ce-express-radio-link) includes ITU-R **availability prediction**:

| Availability | Typical Use |
|-------------|------------|
| 99.999% | Critical infrastructure (telecom backhaul) |
| 99.99% | High-availability links |
| 99.9% | Standard commercial links |

## Reflections

The **Reflections** tab analyses signal reflections from terrain+topography) and water bodies that can cause multipath interference on the link.

## Link Prediction Report

Click **Export+raster+vector)** → generates a PDF report with:
- Link parameters summary
- Path profile+microwave+link)
- [Link budget](#kw:link-budget-calculation:ce-express-radio-link) table
- Availability calculation
- [Fade margin](#ce-express-radio-link) analysis

## Multi-Hop Paths

For multi-hop backhaul:
1. Create links between consecutive sites
2. CE Express calculates end-to-end performance for each hop
3. Total availability = product of individual hop availabilities

## MW Equipment Library

→ See [MW Equipment →](#ce-express-mw-equipment)

To use Link Prediction, assign antenna and radio models from the equipment library to each link endpoint.

## Automatic Frequency Planning (AFP)

For mesh and multi-link networks, use **AFP** to automatically assign frequencies minimizing interference.

→ See [Automatic Frequency Planning →](#ce-express-afp)

## Related Topics

- [Profile / Line of Sight →](#ce-express-profile)
- [MW Equipment Library →](#ce-express-mw-equipment)
- [Mesh Networks →](#ce-express-mesh)
