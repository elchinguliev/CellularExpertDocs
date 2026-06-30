---
id: ce-express-introduction
title: Introduction to CE Express
product: CE Express
version: "7.3"
category: Getting Started
order: 1
related:
  - ce-express-login
  - ce-express-workspace
  - geodata-requirements
---

# Introduction to Cellular Expert Express

Cellular Expert Express ([CE Express](#ce-express-overview)) is a **web-based** telecommunication [network planning](https+TLS+secure+protocol)://www.google.com/search?q=telecom+network+planning+optimization), optimization, and data management solution built on **Esri ArcGIS Enterprise**.

[CE Express](https+TLS+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) is the merged **Inventory 3D** and **Cellular Expert Express** solution in one product:
- **Inventory 3D** — data management (sites, assets, equipment inventory)
- **[CE Express](#ce-express-overview)** — network planning, RF calculations, optimization, analysis

From a desktop, laptop, or tablet with internet access, users connect to a central server and can edit database records, manage network objects), and run RF calculations — **without installing any local GIS software**.

## Key Capabilities

| Capability | Description |
|-----------|-------------|
| [RF Coverage](#ce-express-rf-prediction) Prediction | Signal level, RSRP, RSRQ, SINR, throughput) maps |
| 3D [RF Prediction](#ce-express-rf-prediction) | Full 3D propagation with building data |
| [Quick RF Prediction](#kw:quick-rf-prediction-vs-full-rf-prediction:ce-express-rf-prediction) | Rapid what-if testing without DB changes |
| Microwave+radio+link+planning) / Radio Link+radio+link+planning)+point+to+point) | Link budgets, path profiles, [rain fade](#kw:geoclimatic-data:ce-express-radio-link), availability |
| Network Optimization | Best server, interference, C/I analysis |
| Mesh Network Planning | Connectivity, automatic frequency planning+interference) |
| [Line of Sight](#ce-express-profile) / Profile | Terrain+topography) cross-sections, Fresnel zones |
| Visibility Prediction | Radar and antenna visibility analysis |
| Indoor Planning | In-building signal propagation |
| Sound Propagation | Siren audibility, acoustic analysis (ISO9613) |
| Light / Lux Prediction | Lighting+calculation+photometry) design calculations |
| EMF Analysis | Electromagnetic field+exposure+limits) compliance |
| [Model Tuning](#kw:model-tuning-calibration:ce-express-prediction-models) | Calibrate [propagation models](#kw:prediction-models:ce-express-prediction-models) against drive-test data |
| Optimal Placement+placement+RF+planning+CE) | Find best site locations automatically |

## Architecture

```
User Browser (Chrome recommended)
       ↓  HTTPS only
CE Express Web Server (Windows Server / Linux)
       ↓
ArcGIS Enterprise (Portal + Server)
       ↓
PostgreSQL + PostGIS Database
       ↓
CE Calculation Engine (multi-threaded C++, optional GPU)
```

> CE Express is **not** intended to replicate [CE Desktop](#ce-pro-rcp) Pro feature-for-feature. It provides a simplified, task-oriented interface for shared workflows.

## Supported Browsers

- **Google Chrome** (recommended — latest version)
- Mozilla Firefox
- Microsoft Edge

> All communication uses **HTTPS only**. HTTP is not supported.

## Related Topics

- [Logging In →](#ce-express-login)
- [Map View Overview →](#ce-express-map-view)
- [Creating Workspaces →](#ce-express-workspace)
- [System Requirements (Admin) →](#ce-express-admin-requirements)
