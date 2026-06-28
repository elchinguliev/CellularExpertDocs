# Network Objects

[Network objects]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=radio+network+objects+sites+cells+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)) are the radio infrastructure elements managed in [CE Express]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform): **sites**, **cells**, and **repeaters**. All objects are stored in the [PostgreSQL](https://www.google.com/search?q=PostgreSQL+database+open+source) database and are visible on the map when a [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+workspace+project+geodatabase) is selected.

## Object Types

| Type | Description |
|---|---|
| **[Site](https://www.google.com/search?q=cell+site+tower+base+station+location)** | A physical location (tower, rooftop, pole) that hosts one or more cells |
| **[Cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)** | A single radio [sector](https://www.google.com/search?q=[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+sector+antenna+coverage+area) — one antenna with defined position, direction, frequency, and power |
| **[Repeater](https://www.google.com/search?q=radio+repeater+signal+booster+telecom)** | A signal booster that receives and retransmits a cell's signal |

## Required Cell Attributes

| Attribute | Description |
|---|---|
| `cell_name` | Unique identifier for the cell |
| `latitude` | [WGS84](https://www.google.com/search?q=WGS84+geographic+coordinate+system) decimal degrees (e.g. 54.6872) |
| `longitude` | [WGS84](https://www.google.com/search?q=WGS84+World+Geodetic+System+coordinate) decimal degrees (e.g. 25.2797) |

## Common Optional Attributes

| Attribute | Description |
|---|---|
| `site_name` | Parent [site](https://www.google.com/search?q=cell+site+tower+base+station+location) name |
| `height` | Antenna [height above ground](https://www.google.com/search?q=height+above+ground+[AGL](https://www.google.com/search?q=AGL+Above+Ground+Level+height+measurement)+antenna) (metres) |
| `azimuth` | Horizontal direction the antenna faces (0–360°, clockwise from north) |
| `tilt` | Vertical [downtilt](https://www.google.com/search?q=antenna+downtilt+mechanical+electrical+degrees) angle (degrees) |
| `frequency_mhz` | Operating frequency in [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit) (e.g. 1800, 2100, 3500) |
| `power_dbm` | [Transmit power](https://www.google.com/search?q=transmit+power+[dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit)+radio+antenna) in [dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit) |
| `technology` | Radio technology: `2G`, `3G`, `4G`, or `5G` |
| `antenna_pattern` | Name of the assigned [antenna pattern](https://www.google.com/search?q=antenna+radiation+pattern+format) file |

## Adding Objects Manually

1. Open **Network Data Management** (button in top toolbar).
2. Click **Add New Record**.
3. Fill in `cell_name`, `latitude`, and `longitude` (minimum required).
4. Fill in any additional attributes.
5. Click **Save**.
6. Click **Synchronize Changes** to push to the database and display on the map.

## Importing Objects from CSV

Bulk [import](https://www.google.com/search?q=data+import+GIS+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) is the fastest way to add many cells at once.

1. Open **Network Data Management**.
2. Click **[Import](https://www.google.com/search?q=data+import+GIS+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format))**.
3. Select your CSV file. The file must have a header row with column names matching [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) field names.
4. Map any columns that don't match automatically.
5. Click **Import**.
6. Click **Synchronize Changes** to confirm.

### CSV Template

Minimum required columns:
```
cell_name,latitude,longitude
```

Full template:
```
cell_name,site_name,latitude,longitude,height,azimuth,tilt,frequency_mhz,power_dbm,technology,antenna_pattern
SITE01_A,SITE01,54.6872,25.2797,30,0,3,1800,43,4G,
SITE01_B,SITE01,54.6872,25.2797,30,120,3,1800,43,4G,
SITE01_C,SITE01,54.6872,25.2797,30,240,3,1800,43,4G,
```

> Download the template from the [Downloads](../../downloads.md) page.

## Editing Objects

### On the Map

Click an object to select it. Its attributes appear in the side panel where you can edit them inline.

### In the Table

Switch to Network Data Management, find the row, and click any cell to edit it. Click **Synchronize Changes** when done.

## Moving an Object

1. Select the object on the map.
2. Click the **Move** tool in the toolbar.
3. Click the new position on the map — a yellow dot marks it and coordinates update automatically.
   - Alternatively, type new latitude/longitude values directly.
4. Click **Accept** to confirm.

## Duplicating Objects

1. Select the objects to duplicate (use Rectangle Selection for multiple).
2. Click **Duplicate selected objects**.
3. Choose the target [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase) from the dropdown.
4. Set the new position by clicking the map or entering coordinates.
5. Click **Accept**.

## Deleting Objects

Select the object → right-click → **Delete**, or select the row in Network Data Management and click **Delete Record**.

> In [Inventory3D](https://www.google.com/search?q=Cellular+Expert+Inventory3D+asset+management), permanent deletion requires the **Delete Object Permanently** admin function. Standard deletion in CE Express moves objects to a soft-deleted state.

## Selecting Multiple Objects

Use the **Rectangle Selection** tool to draw a box on the map and select all objects within it. Then use **Show In Table → Cells** to view and bulk-edit their attributes.

## Related Pages

- [Antenna Patterns](antenna-patterns.md) — assigning patterns to cells
- [RF Prediction](rf-prediction.md) — running predictions on selected cells
- [Workspaces](workspace.md) — workspace and database overview
