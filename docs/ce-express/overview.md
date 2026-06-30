# CE Express — Overview

[CE Express](https+TLS+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) is a **web-based radio [network planning](https+TLS+secure+protocol)://www.google.com/search?q=telecom+network+planning+optimization) and optimisation** application built on top of **ArcGIS Enterprise+platform)+Enterprise+server+GIS+deployment)**. It runs entirely in a browser — no desktop software is required for end users.

## What CE Express Does

[CE Express](#ce-express-overview) brings together all of the tools a radio network engineer needs into a single map-based interface:

- **Network object management** — create, edit, import), and organise sites, cells, and repeaters
- **[RF prediction](#ce-express-rf-prediction)** — calculate RSRP), SINR, throughput), and best-server coverage for 4G and 5G networks
- **Path profile+microwave+radio+link+planning)+link) analysis** — check line-of-sight+radio+link) clearance and link budgets between two points
- **Street View** — verify antenna positions and surroundings at ground level
- **[Antenna pattern](#kw:antenna-patterns:ce-express-antenna) management** — import) and assign vendor antenna patterns (.msi / .txt) to cells
- **[Workspace](#kw:creating-a-workspace:ce-express-workspace)+[workspace](#kw:creating-a-workspace:ce-express-workspace)+project+geodatabase) management** — organise projects by workspace, each with its own geodata and prediction settings
- **ArcGIS Portal publishing** — share prediction results as hosted feature layers with your organisation

## Architecture

[CE Express](#ce-express-overview) is deployed on a [Windows Server](#ce-express-admin-requirements) running **ArcGIS Enterprise**. The backend handles all heavy computation (RF predictions, database queries). Users access CE Express through the ArcGIS Enterprise+platform)+Enterprise+server+GIS) portal using their ArcGIS credentials.

```
Browser (user)
    │
    ▼
ArcGIS Enterprise Portal
    │
    ▼
CE Express Web Application
    │
    ├── PostgreSQL Database  (network objects, prediction results)
    ├── Geodata Folder       (elevation.tif, clutter rasters)
    └── Antenna Library      (.msi pattern files)
```

## Key Concepts

| Concept | Description |
|---|---|
| **Workspace** | A project container — links your network objects to a geodata folder and prediction model settings |
| **Cell** | A single radio sector+sector+antenna+coverage+area): one antenna with defined position, azimuth, tilt, frequency, and power |
| **Site** | A physical location (tower, rooftop) that hosts one or more cells |
| **Geodata** | [GeoTIFF](#geodata-[dem](#geodata-dem)) raster files (elevation+height+datum), [clutter](#kw:clutter-classes-grid:geodata-clutter)) used as terrain input for predictions |
| **Prediction** | A calculated coverage output: RSRP+mobile)+4G), SINR), throughput) rasters for a selected set of cells |

## Related Pages

- [Logging In](login.md) — how to access CE Express
- [Workspaces](workspace.md) — creating and configuring workspaces
- [RF Prediction](rf-prediction.md) — running coverage predictions
- [System Requirements](../installation/requirements.md) — server and hardware requirements
