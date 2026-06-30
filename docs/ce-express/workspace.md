# Workspaces

A **[workspace](https+TLS+secure+protocol)://www.google.com/search?q=[ArcGIS](https+TLS+secure+protocol)://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+[workspace](#kw:creating-a-workspace:ce-express-workspace)+project+geodatabase)** is the top-level project container in [CE Express](#ce-express-overview). Each [workspace](#kw:creating-a-workspace:ce-express-workspace)+platform)+workspace+project+geodatabase) links your network objects to a geodata folder (terrain and [clutter](#kw:clutter-classes-grid:geodata-clutter) rasters) and a set of prediction model settings. You must have a workspace selected before you can view objects on the map or run RF predictions.

## What a Workspace Contains

- Network objects (sites, cells, repeaters) stored in the PostgreSQL database
- A reference to the **geodata folder** on the server (elevation+height+datum).tif, [clutter](#kw:clutter-classes-grid:geodata-clutter) files)
- The **coordinate reference system (CRS)** for that project area
- Assigned **prediction model** configurations

## Opening the Workspace Tool

Click the **Workspace** icon in the left toolbar of Map View.

## Selecting a Workspace

1. Open the Workspace tool.
2. Click on a workspace name to select it.
3. The map loads all network objects from that workspace.

> If no workspaces appear, contact your administrator — workspaces must be created and shared with your ArcGIS+platform) user account.

## Creating a New Workspace

1. Open the Workspace tool.
2. Click **Create New Workspace**.
3. Fill in the fields:

| Field | Description |
|---|---|
| **Name** | A descriptive name for the project (e.g. "Vilnius 4G Q1 2025") |
| **Geodata folder** | Server path to the folder containing `elevation.tif` and optional clutter rasters |
| **Coordinate system** | Must match the CRS of your [GeoTIFF](#geodata-[dem](#geodata-dem)) rasters (Projected CRS, not geographic/WGS84) |

4. Click **Save**.

## Duplicating a Workspace

Duplicating is useful when you want to test changes without affecting an existing project.

1. Open the Workspace tool.
2. Hover over the workspace you want to copy — three icons appear on the right.
3. Click the **Duplicate** icon (two overlapping pages).
4. Enter a name for the new workspace.
5. Click **OK**.

> If the new workspace does not appear immediately, refresh the page.

The duplicate inherits all settings from the original. Network objects are **not** copied — both workspaces read from the same database table. To work on a separate copy of the objects, use the Import)/Export tools.

## Editing Workspace Settings

1. Hover over the workspace → click the **Settings** icon (gear).
2. Update the geodata folder path or coordinate system as needed.
3. Click **Save**.

## Deleting a Workspace

1. Hover over the workspace → click the **Delete** icon (bin).
2. Confirm deletion.

> Deleting a workspace does **not** delete the network objects in the database — only the workspace container and its settings are removed.

## Related Pages

- [Geodata & Rasters](geodata.md) — preparing elevation.tif and clutter files
- [RF Prediction](rf-prediction.md) — prediction model settings
- [Network Objects](network-objects.md) — managing sites and cells within a workspace
