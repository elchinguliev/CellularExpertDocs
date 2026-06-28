---
id: ce-express-admin-requirements
title: System Requirements
product: CE Express
version: "7.2"
category: Administration
order: 20
related:
  - ce-express-admin-installation
  - ce-express-admin-user-management
---

# __S1__ System Requirements

## Minimum Hardware Requirements

### Server (CE Express + __S2__+Enterprise+server+deployment))

| Component | Minimum | Recommended | Optimal |
|-----------|---------|-------------|---------|
| **CPU** | 8 cores, hyperthreaded | 16 cores | 32 cores |
| **RAM** | 16 GB | 32 GB | 64 GB or more |
| **Storage** | 500 GB – 1 TB free | 2 TB+ SSD | NVMe SSD RAID |

### Optional: __S3__-Accelerated Calculations

| Component | Requirement |
|-----------|------------|
| [GPU](https://www.google.com/search?q=GPU+graphics+processing+unit) | Any [NVIDIA](https://www.google.com/search?q=NVIDIA+GPU+computing) [GPU](https://www.google.com/search?q=GPU+graphics+processing+unit+computing) with [CUDA](https://www.google.com/search?q=NVIDIA+CUDA+parallel+computing+platform) capabilities |
| Driver | Version 456.38 or later |
| [CUDA](https://www.google.com/search?q=NVIDIA+CUDA+parallel+computing) Toolkit | 11.0 – 12.4 (recommended) |

See: [https://developer.nvidia.com/cuda-gpus](https://developer.nvidia.com/cuda-gpus)

> Requirements vary significantly depending on acceptable calculation time, task complexity, and database size.

## Minimum Software Requirements

| Software | Version | Notes |
|----------|---------|-------|
| **Operating System** | [Windows Server](https://www.google.com/search?q=Windows+Server+Microsoft+operating+system) 2016/2019/2022 | Also supported: [Ubuntu](https://www.google.com/search?q=Ubuntu+Linux+server+operating+system) 20.04+ |
| **[ArcGIS Server]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=[ArcGIS]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+Server+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+web+services)** | 10.9.1 or later | Required for map services |
| **[ArcGIS Portal](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+Portal+enterprise+web+GIS)** | 10.9.1 or later | Required for user authentication |
| **[PostgreSQL](https://www.google.com/search?q=PostgreSQL+database+open+source)** | 13 or later | With [PostGIS](https://www.google.com/search?q=PostGIS+PostgreSQL+spatial+extension) extension |
| **[PHP](https://www.google.com/search?q=PHP+server+side+scripting+language) Server** | 7.4 or later | For [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) web application |
| **Web Server** | [IIS](https://www.google.com/search?q=Microsoft+IIS+web+server) (Windows) or [Nginx](https://www.google.com/search?q=Nginx+web+server) ([Linux](https://www.google.com/search?q=Linux+operating+system+server)) | Front-end proxy |

## Architecture Examples

### Simplified On-Premises Deployment

```
[User Browser]
      ↓ HTTPS
[IIS / Nginx Web Server]
      ↓
[CE Express Application + PHP]
      ↓
[ArcGIS Enterprise (Portal + Server)]
      ↓
[PostgreSQL + PostGIS Database]
      ↓
[CE Calculation Engine]
```

### Cloud / Hybrid Deployment

[CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) supports cloud deployment on:
- **Microsoft Azure** (recommended)
- **AWS**
- **Google Cloud Platform**

[ArcGIS Enterprise](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+Enterprise+server+GIS) and the CE Express server can be on separate machines/VMs.

## Related Topics

- [Installation Guide →](#ce-express-admin-installation)
- [Geodata Preparation (Admin) →](#ce-express-admin-geodata)
- [User Management →](#ce-express-admin-user-management)
