---
id: ce-express-profile
title: Line of Sight and Profile Analysis
product: CE Express
version: "7.3"
category: Calculations
order: 8
related:
  - ce-express-rf-prediction
  - ce-express-radio-link
  - geodata-requirements
---

# __S0__ and Profile Analysis

The **Profile** tool computes [terrain]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography) cross-sections and checks whether two points have a clear radio path.

## Opening the Profile Tool

Click **Profile** in the left toolbar.

## Drawing a Profile

1. Click **Draw Profile** in the tool panel
2. Click two points on the map (start and end)
3. [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) computes the [terrain profile]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=[terrain](https://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography)+profile+[elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum)+radio+link) using the loaded [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain)

Alternatively:
- Select two existing [network objects](https://www.google.com/search?q=radio+network+objects+sites+cells+GIS) → Profile is drawn between them
- [Import](https://www.google.com/search?q=data+import+GIS+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) profile endpoints from a file

## Profile Properties

Configure before drawing:

| Property | Description |
|----------|-------------|
| **Frequency ([MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit))** | Affects [Fresnel zone](https://www.google.com/search?q=Fresnel+zone+radio+link+clearance) radius calculation |
| **[K-factor](https://www.google.com/search?q=K+factor+earth+bulge+radio+propagation)** | Earth curvature correction. Default: 4/3 (standard atmosphere). Use 2/3 for worst-case [diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation). |
| **Antenna height A** | Height at start point (m [AGL](https://www.google.com/search?q=AGL+Above+Ground+Level+height+measurement)) |
| **Antenna height B** | Height at end point (m [AGL](https://www.google.com/search?q=AGL+Above+Ground+Level+height+measurement)) |
| **[DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster) source** | Terrain dataset to use |

## Profile Results

The profile chart shows:

| Element | Description |
|---------|-------------|
| **Terrain cross-section** | [Elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum) profile along the path |
| **[Line of sight](https://www.google.com/search?q=Line+of+Sight+[LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation)+radio+propagation)** | Direct path between antennas |
| **Fresnel zones** | 1st (and higher) [Fresnel zone](https://www.google.com/search?q=Fresnel+zone+radio+link+clearance) ellipses |
| **[Earth bulge](https://www.google.com/search?q=earth+bulge+curvature+radio+link)** | Earth curvature correction (based on [K-factor](https://www.google.com/search?q=K+factor+earth+bulge+radio+propagation)) |
| **Obstacles** | Terrain or building obstructions |
| **Clearance** | Vertical clearance above terrain at critical points |

## Result Interpretation

| Indicator | Meaning |
|-----------|---------|
| 🟢 Green | Clear [LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation) — 1st [Fresnel zone](https://www.google.com/search?q=Fresnel+zone+radio+link+clearance+calculation) fully clear |
| 🟡 Yellow | Marginal — 1st [Fresnel zone](https://www.google.com/search?q=Fresnel+zone+radio+link+clearance+calculation) partially obstructed |
| 🔴 Red | Obstructed — direct path blocked |

> For [microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning) links, the 1st Fresnel zone should be **at least 60% clear** for acceptable performance.

## Profile Tools

- **Zoom** — zoom in/out on the profile chart
- **Pan** — pan along the profile
- **Measure** — measure distances and heights on the profile

## Exporting the Profile

Click **[Export](https://www.google.com/search?q=data+export+GIS+raster+vector)** (Profile Report) to generate a PDF report containing:
- Profile chart
- Fresnel zone analysis
- Link parameters summary
- Clearance table

## Settings

Configure display options:
- Show/hide Fresnel zones (1st, 2nd, nth)
- Color scheme
- Grid display

## Import

[Import](https://www.google.com/search?q=data+import+GIS+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) profile endpoints from coordinates ([CSV](https://www.google.com/search?q=CSV+comma-separated+values+file+format)) or from existing [network objects](https://www.google.com/search?q=radio+network+objects+sites+cells+GIS).

## Related Topics

- [Radio Link Prediction →](#ce-express-radio-link)
- [RF Prediction →](#ce-express-rf-prediction)
- [Geodata Requirements →](#geodata-requirements)
