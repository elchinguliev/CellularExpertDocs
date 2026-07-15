# Radar Prediction

> **Version:** CE Pro v4.9

## Overview

Radar Prediction calculates the detection reach of radar signals across an area. The tool accounts for terrain (DTM), obstacles, and the radar cross-section of different target types. Detection range varies by target — drones are identified within a shorter distance than aircraft.

![Map view showing radar prediction coverage results](https://doc.esri.com/en/arcgis-pro/latest/get-started/images/arcgis-pro-view-AFCF6.png)

---

## How to Run

1. Click the **Radar Prediction** button in the CE Desktop tab
2. The Radar Prediction dialogue opens
3. Set the parameters below
4. Click **Run Calculation**

---

## Parameters

| Parameter | Description |
|-----------|-------------|
| Calculation name | Unique name to identify this prediction result |
| Resolution | Cell size of the output raster, in metres |
| Best Server count | Calculate up to 5 best servers (radar sources) |
| Radar template | Pre-configured template defining radar specifications |
| Target cross-section | Radar cross-section (RCS) of the target — affects detection range. Drones have a smaller RCS than aircraft |
| Selected | Number of radar objects currently selected on the map |

---

## Results

The output is a raster layer added to the map:

- **Field Strength raster** — signal level in dBm across the coverage area
- Higher values indicate stronger radar detection at that location
- Areas below detection threshold appear as no-data or a separate colour class

---

## Use Cases

- Airport and airspace surveillance coverage planning
- Drone detection zone mapping
- Military and defence radar network design
- Identifying gaps in radar coverage requiring additional sensors
