---
id: training-ce-express-workspace
title: "Training 01: Creating a Workspace (CE Express)"
product: CE Express
category: Training
order: 1
related:
  - ce-express-workspace
  - ce-express-login
  - geodata-requirements
---

# Training Module 01 — Creating a Workspace in CE Express

**Duration:** ~1 hour | **Level:** Beginner

## Objectives

By the end of this module, you will be able to:

- Create and configure a [workspace]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=[ArcGIS]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+workspace+project+geodatabase) correctly in [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform)
- Understand [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+workspace+project+geodatabase) structure and scope
- Manage and visualize layers efficiently
- Switch between 2D and 3D environments
- Prepare a workspace for RF planning tasks

## Initial Data

For this exercise, the following is pre-configured:
- Prepared geodata (high-[resolution](https://www.google.com/search?q=spatial+resolution+[raster](https://www.google.com/search?q=raster+GIS+grid+data+format)+GIS+accuracy) [terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) and [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio))
- Predefined external services for visualization

> **Trainer note:** Emphasize that workspace quality directly affects prediction accuracy, visualization clarity, and collaboration efficiency.

## Understanding the Workspace Concept

A **Workspace** in [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) is a project container holding:

- [Network objects](https://www.google.com/search?q=radio+network+objects+sites+cells+GIS) (sites, cells, links, etc.)
- Geodata for propagation modeling
- Visualization layers ([GIS](https://www.google.com/search?q=GIS+Geographic+Information+System), 3D meshes, administrative boundaries)

Workspaces can be:
- Assigned to one or multiple user groups
- Used collaboratively by RF planners, optimization engineers, and managers
- Reused as templates for similar geographic areas

**→ For full workspace documentation, see [Workspaces →](#ce-express-workspace)**

## Step 1 — Accessing CE Express

1. Open the following URL in your browser: `https://cecom2.cellular-expert.com/ce_express/`
2. On the login page, select **Login as ArcGIS**
3. Enter your Username and Password (provided separately per student)
4. After authentication, the system displays all workspaces available to your user group

> **Best practice:** Always verify you are working in the correct workspace before making changes.

## Step 2 — Creating a New Workspace

1. Click the **Workspaces** tool in the left toolbar
2. Click **New workspace**
3. Fill in workspace parameters:

| Field | Value for this exercise |
|-------|------------------------|
| Workspace name | `Training_[YourName]` |
| [Coordinate system](https://www.google.com/search?q=coordinate+reference+system+CRS+GIS) [EPSG](https://www.google.com/search?q=EPSG+coordinate+reference+system) | [EPSG](https://www.google.com/search?q=EPSG+coordinate+reference+system+code+database) for your training area (instructor provides) |
| Group | `Training` |

4. Set the **extent** by clicking **Draw on map** and drawing a rectangle around your planning area
5. Select the **Geodata set** prepared for this exercise
6. Click **Save**

## Step 3 — Exploring the Map View

After creating the workspace, explore the map view:

1. The map auto-zooms to the workspace extent
2. Confirm the [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain)/[terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) is visible (enable in Layers if not)
3. Check that [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) layer is loaded

## Step 4 — Adding an Extra Layer

1. In workspace settings → Extra layers → click **Add layer**
2. Enter an [ArcGIS Portal](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+Portal+enterprise+web+GIS) Item ID or URL for a background map
3. Set opacity to 70%
4. Click Save

## Step 5 — Switching Between Workspaces

1. Click the Workspaces tool
2. Click another workspace in the list
3. Observe that the map zooms to the new workspace extent
4. Switch back to your training workspace

## Exercise

Create a workspace for a new planning project:
- Name: `[YourName]_Exercise_01`
- Area: 50 km × 50 km urban area
- [Coordinate system](https://www.google.com/search?q=coordinate+reference+system+CRS+GIS): [UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator) (ask instructor for local [UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator+projection) zone)
- Load [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster) and [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) geodata set
- Add an OpenStreetMap background layer

## Related Documentation

- **Full workspace documentation:** [Workspaces →](#ce-express-workspace)
- **Geodata requirements:** [Geodata Requirements →](#geodata-requirements)
- **Login help:** [Logging In →](#ce-express-login)
