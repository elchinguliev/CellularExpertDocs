# Workspaces

A **[workspace]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=[ArcGIS]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+workspace+project+geodatabase)** is the top-level project container in [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform). Each [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+workspace+project+geodatabase) links your [network objects](https://www.google.com/search?q=radio+network+objects+sites+cells+GIS) to a geodata folder ([terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) and [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio) rasters) and a set of prediction model settings. You must have a workspace selected before you can view objects on the map or run RF predictions.

## What a Workspace Contains

- [Network objects](https://www.google.com/search?q=radio+network+objects+sites+cells+GIS) (sites, cells, repeaters) stored in the [PostgreSQL](https://www.google.com/search?q=PostgreSQL+database+open+source) database
- A reference to the **geodata folder** on the server ([elevation](https://www.google.com/search?q=elevation+model+[terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography)+height+datum).tif, [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) files)
- The **coordinate reference system (CRS)** for that project area
- Assigned **prediction model** configurations

## Opening the Workspace Tool

Click the **Workspace** icon in the left toolbar of Map View.

## Selecting a Workspace

1. Open the Workspace tool.
2. Click on a workspace name to select it.
3. The map loads all network objects from that workspace.

> If no workspaces appear, contact your administrator — workspaces must be created and shared with your [ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform) user account.

## Creating a New Workspace

1. Open the Workspace tool.
2. Click **Create New Workspace**.
3. Fill in the fields:

| Field | Description |
|---|---|
| **Name** | A descriptive name for the project (e.g. "Vilnius [4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology) Q1 2025") |
| **Geodata folder** | Server path to the folder containing `elevation.tif` and optional [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) rasters |
| **[Coordinate system](https://www.google.com/search?q=coordinate+reference+system+CRS+GIS)** | Must match the CRS of your [GeoTIFF](https://www.google.com/search?q=GeoTIFF+raster+geospatial+format) rasters (Projected CRS, not geographic/[WGS84](https://www.google.com/search?q=WGS84+geographic+coordinate+system)) |

4. Click **Save**.

## Duplicating a Workspace

Duplicating is useful when you want to test changes without affecting an existing project.

1. Open the Workspace tool.
2. Hover over the workspace you want to copy — three icons appear on the right.
3. Click the **Duplicate** icon (two overlapping pages).
4. Enter a name for the new workspace.
5. Click **OK**.

> If the new workspace does not appear immediately, refresh the page.

The duplicate inherits all settings from the original. Network objects are **not** copied — both workspaces read from the same database table. To work on a separate copy of the objects, use the [Import](https://www.google.com/search?q=data+import+GIS+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format))/[Export](https://www.google.com/search?q=data+export+GIS+raster+vector) tools.

## Editing Workspace Settings

1. Hover over the workspace → click the **Settings** icon (gear).
2. Update the geodata folder path or [coordinate system](https://www.google.com/search?q=coordinate+reference+system+CRS+GIS) as needed.
3. Click **Save**.

## Deleting a Workspace

1. Hover over the workspace → click the **Delete** icon (bin).
2. Confirm deletion.

> Deleting a workspace does **not** delete the network objects in the database — only the workspace container and its settings are removed.

## Related Pages

- [Geodata & Rasters](geodata.md) — preparing [elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum).tif and clutter files
- [RF Prediction](rf-prediction.md) — prediction model settings
- [Network Objects](network-objects.md) — managing sites and cells within a workspace
