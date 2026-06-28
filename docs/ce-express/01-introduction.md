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

Cellular Expert Express ([CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform)) is a **web-based** telecommunication [network planning]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=telecom+network+planning+optimization), optimization, and data management solution built on **Esri [ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform) Enterprise**.

[CE Express]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) is the merged **Inventory 3D** and **Cellular Expert Express** solution in one product:
- **Inventory 3D** — data management (sites, assets, equipment inventory)
- **[CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform)** — [network planning](https://www.google.com/search?q=telecom+network+planning+optimization), RF calculations, optimization, analysis

From a desktop, laptop, or tablet with internet access, users connect to a central server and can edit database records, manage [network objects](https://www.google.com/search?q=radio+network+objects+sites+cells+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)), and run RF calculations — **without installing any local [GIS](https://www.google.com/search?q=GIS+Geographic+Information+System) software**.

## Key Capabilities

| Capability | Description |
|-----------|-------------|
| RF [Coverage Prediction](https://www.google.com/search?q=coverage+prediction+RF+radio+planning) | Signal level, [RSRP](https://www.google.com/search?q=RSRP+Reference+Signal+Received+Power+LTE+4G), [RSRQ](https://www.google.com/search?q=RSRQ+Reference+Signal+Received+Quality+LTE+4G), [SINR](https://www.google.com/search?q=SINR+Signal+to+Interference+Noise+Ratio), [throughput](https://www.google.com/search?q=network+throughput+downlink+uplink+[capacity](https://www.google.com/search?q=network+capacity+planning+telecom)) maps |
| 3D [RF Prediction](https://www.google.com/search?q=RF+radio+frequency+prediction+coverage+planning) | Full 3D propagation with building data |
| [Quick RF Prediction](https://www.google.com/search?q=Quick+RF+Prediction+what+if+testing+CE+Express) | Rapid what-if testing without [DB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit) changes |
| [Microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning) / [Radio Link](https://www.google.com/search?q=radio+link+[microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning)+point+to+point) | Link budgets, path profiles, [rain fade](https://www.google.com/search?q=rain+fade+attenuation+microwave+link), [availability](https://www.google.com/search?q=link+availability+percentage+microwave+ITU) |
| Network Optimization | [Best server](https://www.google.com/search?q=best+server+analysis+coverage+planning+RF), [interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent), C/I analysis |
| [Mesh Network](https://www.google.com/search?q=mesh+network+wireless+topology) Planning | Connectivity, [automatic frequency planning](https://www.google.com/search?q=Automatic+Frequency+Planning+[AFP](https://www.google.com/search?q=Automatic+Frequency+Planning+radio+network)+[interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent)) |
| [Line of Sight](https://www.google.com/search?q=Line+of+Sight+LOS+radio+propagation) / Profile | [Terrain](https://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography) cross-sections, Fresnel zones |
| Visibility Prediction | Radar and antenna visibility analysis |
| Indoor Planning | In-building [signal propagation](https://www.google.com/search?q=signal+propagation+radio+wave) |
| Sound Propagation | [Siren](https://www.google.com/search?q=siren+audibility+sound+propagation+ISO9613) audibility, [acoustic](https://www.google.com/search?q=acoustic+propagation+sound+wave+modeling) analysis ([ISO9613](https://www.google.com/search?q=ISO+9613+acoustic+propagation+standard)) |
| Light / [Lux](https://www.google.com/search?q=lux+light+intensity+measurement+unit) Prediction | [Lighting](https://www.google.com/search?q=lighting+design+[lux](https://www.google.com/search?q=lux+light+intensity+measurement+unit)+calculation+photometry) design calculations |
| [EMF](https://www.google.com/search?q=EMF+electromagnetic+field+exposure+assessment) Analysis | [Electromagnetic field](https://www.google.com/search?q=electromagnetic+field+[EMF](https://www.google.com/search?q=EMF+electromagnetic+field+exposure+assessment)+exposure+limits) compliance |
| [Model Tuning](https://www.google.com/search?q=propagation+model+tuning+calibration+drive+test) | Calibrate [propagation models](https://www.google.com/search?q=radio+propagation+models+comparison+telecom) against drive-test data |
| [Optimal Placement](https://www.google.com/search?q=optimal+[site](https://www.google.com/search?q=cell+site+tower+base+station+location)+placement+RF+planning+CE) | Find best [site](https://www.google.com/search?q=cell+site+tower+base+station+location) locations automatically |

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

> CE Express is **not** intended to replicate [CE Desktop](https://www.google.com/search?q=Cellular+Expert+CE+Desktop+ArcGIS+Pro) Pro feature-for-feature. It provides a simplified, task-oriented interface for shared workflows.

## Supported Browsers

- **[Google Chrome](https://www.google.com/search?q=Google+Chrome+web+browser)** (recommended — latest version)
- Mozilla [Firefox](https://www.google.com/search?q=Mozilla+Firefox+web+browser)
- Microsoft Edge

> All communication uses **HTTPS only**. [HTTP](https://www.google.com/search?q=HTTP+HyperText+Transfer+Protocol) is not supported.

## Related Topics

- [Logging In →](#ce-express-login)
- [Map View Overview →](#ce-express-map-view)
- [Creating Workspaces →](#ce-express-workspace)
- [System Requirements (Admin) →](#ce-express-admin-requirements)
