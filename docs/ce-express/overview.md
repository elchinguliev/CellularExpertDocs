# CE Express — Overview

[CE Express]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) is a **web-based radio [network planning]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=telecom+network+planning+optimization) and optimisation** application built on top of **[ArcGIS Enterprise](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+Enterprise+server+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+deployment)**. It runs entirely in a browser — no desktop software is required for end users.

## What CE Express Does

[CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) brings together all of the tools a radio network engineer needs into a single map-based interface:

- **[Network object](https://www.google.com/search?q=radio+network+object+GIS+database) management** — create, edit, [import](https://www.google.com/search?q=data+import+GIS+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)), and organise sites, cells, and repeaters
- **[RF prediction](https://www.google.com/search?q=RF+radio+frequency+prediction+coverage+planning)** — calculate [RSRP](https://www.google.com/search?q=RSRP+Reference+Signal+Received+Power+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+4G)), [SINR](https://www.google.com/search?q=SINR+Signal+Interference+Noise+Ratio), [throughput](https://www.google.com/search?q=network+throughput+downlink+uplink+[capacity](https://www.google.com/search?q=network+capacity+planning+telecom)), and best-server coverage for [4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology) and [5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network) networks
- **[Path profile](https://www.google.com/search?q=path+profile+[terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography)+[microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning)+link) analysis** — check [line-of-sight](https://www.google.com/search?q=line+of+sight+[LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation)+radio+link) clearance and link budgets between two points
- **Street View** — verify antenna positions and surroundings at ground level
- **[Antenna pattern](https://www.google.com/search?q=antenna+radiation+pattern+file+format+MSI) management** — [import](https://www.google.com/search?q=data+import+GIS+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) and assign vendor antenna patterns (.msi / .txt) to cells
- **[Workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase) management** — organise projects by [workspace](https://www.google.com/search?q=ArcGIS+workspace+project+geodatabase), each with its own geodata and prediction settings
- **[ArcGIS Portal](https://www.google.com/search?q=ArcGIS+Portal+enterprise+web+GIS) publishing** — share prediction results as hosted feature layers with your organisation

## Architecture

CE Express is deployed on a [Windows Server](https://www.google.com/search?q=Windows+Server+Microsoft+operating+system) running **[ArcGIS Enterprise](https://www.google.com/search?q=ArcGIS+Enterprise+server+GIS+deployment)**. The backend handles all heavy computation (RF predictions, database queries). Users access CE Express through the [ArcGIS Enterprise](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+Enterprise+server+GIS) portal using their ArcGIS credentials.

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
| **Workspace** | A project container — links your [network objects](https://www.google.com/search?q=radio+network+objects+sites+cells+GIS) to a geodata folder and prediction model settings |
| **[Cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)** | A single radio [sector](https://www.google.com/search?q=[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+sector+antenna+coverage+area): one antenna with defined position, [azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north), tilt, frequency, and power |
| **[Site](https://www.google.com/search?q=cell+site+tower+base+station+location)** | A physical location (tower, rooftop) that hosts one or more cells |
| **Geodata** | [GeoTIFF](https://www.google.com/search?q=GeoTIFF+raster+geospatial+format) [raster](https://www.google.com/search?q=raster+GIS+grid+data+format) files ([elevation](https://www.google.com/search?q=elevation+model+[terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography)+height+datum), [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio)) used as terrain input for predictions |
| **Prediction** | A calculated coverage output: [RSRP](https://www.google.com/search?q=RSRP+Reference+Signal+Received+Power+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+[4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)+mobile)+4G), [SINR](https://www.google.com/search?q=SINR+signal+interference+noise+ratio+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+4G+mobile)), [throughput](https://www.google.com/search?q=network+throughput+downlink+uplink+[capacity](https://www.google.com/search?q=network+capacity+planning+telecom)) rasters for a selected set of cells |

## Related Pages

- [Logging In](login.md) — how to access CE Express
- [Workspaces](workspace.md) — creating and configuring workspaces
- [RF Prediction](rf-prediction.md) — running coverage predictions
- [System Requirements](../installation/requirements.md) — server and hardware requirements
