---
id: ce-express-features
title: Features — Adding and Managing Network Objects
product: CE Express
version: "7.3"
category: Network Objects
order: 5
related:
  - ce-express-workspace
  - network-object-requirements
  - ce-express-rf-prediction
---

# Features Tool

The **Features** tool is used to [import]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=data+import+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)), add, select, and edit all [network objects]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=radio+network+objects+sites+cells+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)) on the map.

Click the **Features** button in the left toolbar to open the tool.

## Importing Features

Click **[Import](https://www.google.com/search?q=data+import+GIS+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) features** to create objects from a file.

### Supported Formats

- **CSV** — comma-separated values
- **[KMZ](https://www.google.com/search?q=KMZ+Google+Earth+file+format)** — Google Earth format

### Import Steps

1. Click **Import features**
2. Select the **object type** ([Site](https://www.google.com/search?q=cell+site+tower+base+station+location), [Cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station), [Repeater](https://www.google.com/search?q=radio+repeater+signal+booster+telecom), Mesh Node, etc.)
3. Select or drag-and-drop your [CSV](https://www.google.com/search?q=CSV+comma-separated+values+file+format) or [KMZ](https://www.google.com/search?q=KMZ+Google+Earth+file+format) file
4. Map columns using the **Mapping** feature if field names differ from CE format
5. Click **Import** — objects appear on the map automatically

### Column Mapping

Enable **Use mapping** to align your file's field names with CE database fields:

| Field | Description |
|-------|-------------|
| **Source** | Column name in your data file |
| **Fill** | Default value when the field is empty in the file |

**Mapping Presets:** Save frequently used mappings as presets → click **New mapping preset** → name it → apply next time automatically.

---

## Adding Features (Manual)

Click **Add features** → select object type → place on map.

Objects can be created:
- From **feature set templates** (pre-configured groups)
- From **zero** (define all parameters manually)

### Feature Set Templates

A feature set template saves a group of related features (e.g., a 3-[sector](https://www.google.com/search?q=[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+sector+antenna+coverage+area) [site](https://www.google.com/search?q=cell+site+tower+base+station+location) with typical parameters) so they can be placed with a single click.

**Quick Add:** If you have templates marked as favorites, they appear in the Quick Add section — drag and drop directly onto the map to place.

---

## Network Object Types

### Site

A physical tower or mast location.

**Required:**
- Site name (unique identifier)
- X coordinate (projected)
- Y coordinate (projected)

**Optional:**
- Height above [terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) (m)

### Cell

A radio [sector](https://www.google.com/search?q=cell+sector+antenna+coverage+area) or cell on a site.

**Required:** Cell name, X, Y, [Azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north) (0–360°, direction from North)

**Optional parameters:**

| Parameter | Unit | Description |
|-----------|------|-------------|
| Height | m | Height above [terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) |
| [Downtilt](https://www.google.com/search?q=antenna+downtilt+mechanical+electrical+degrees) | deg | [Mechanical tilt](https://www.google.com/search?q=mechanical+tilt+antenna+[downtilt](https://www.google.com/search?q=antenna+downtilt+mechanical+electrical+degrees)) |
| El. Downtilt | deg | [Electrical tilt](https://www.google.com/search?q=electrical+tilt+antenna+RET) |
| Frequency | [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit) | [Carrier frequency](https://www.google.com/search?q=carrier+frequency+radio+transmission) |
| Power | [dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit) | [Transmit power](https://www.google.com/search?q=transmit+power+[dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit)+radio+antenna) |
| Misc. loss | [dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit) | Cable and connector losses |
| [Bandwidth](https://www.google.com/search?q=channel+bandwidth+radio+frequency+[MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit)) | MHz | Required for [4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)/[5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network). Use 0.015 for [2G](https://www.google.com/search?q=2G+GSM+mobile+network+second+generation)/[3G](https://www.google.com/search?q=3G+UMTS+HSPA+mobile+network). |
| [Noise figure](https://www.google.com/search?q=noise+figure+receiver+[sensitivity](https://www.google.com/search?q=receiver+sensitivity+dBm+radio)+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit)) | dB | Required for [4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)/[5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network) |
| Downlink duplex factor | 0–1 | For [TDD](https://www.google.com/search?q=TDD+Time+Division+Duplex+LTE+5G) (4G/5G). 0.7 = 70% DL, 30% UL. |
| [Subcarrier spacing](https://www.google.com/search?q=[subcarrier](https://www.google.com/search?q=subcarrier+spacing+[OFDM](https://www.google.com/search?q=OFDM+Orthogonal+Frequency+Division+Multiplexing)+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+4G+mobile)+5G)+spacing+[OFDM](https://www.google.com/search?q=OFDM+Orthogonal+Frequency+Division+Multiplexing)+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+4G+mobile)+5G+[kHz](https://www.google.com/search?q=kHz+kilohertz+frequency+unit)) | [kHz](https://www.google.com/search?q=kHz+kilohertz+frequency+unit) | Required for 4G/5G. Use 15 for [2G](https://www.google.com/search?q=2G+GSM+mobile+network+second+generation)/[3G](https://www.google.com/search?q=3G+UMTS+HSPA+mobile+network). |
| Tx [MIMO](https://www.google.com/search?q=MIMO+Multiple+Input+Multiple+Output+antenna) | — | 1, 2, 4, 8, 16, 32, or 64 |
| Rx [MIMO](https://www.google.com/search?q=MIMO+Multiple+Input+Output+antenna) | — | 1, 2, 4, 8, 16, 32, or 64 |
| Active antenna effect | dB | For [massive MIMO](https://www.google.com/search?q=massive+[MIMO](https://www.google.com/search?q=MIMO+Multiple+Input+Multiple+Output+antenna+technology)+5G+antenna+[beamforming](https://www.google.com/search?q=beamforming+antenna+5G+[MIMO](https://www.google.com/search?q=MIMO+Multiple+Input+Multiple+Output+antenna+technology)+technology)). MIMO 32×32: use 6. MIMO 64×64: use 9. |
| Cell load | % | 0–100. Higher load = lower DL [throughput](https://www.google.com/search?q=network+throughput+downlink+uplink+[capacity](https://www.google.com/search?q=network+capacity+planning+telecom)). |
| Technology | — | 2G, 3G, 4G, or 5G |
| Duplex mode | [FDD](https://www.google.com/search?q=FDD+Frequency+Division+Duplex+LTE)/[TDD](https://www.google.com/search?q=TDD+Time+Division+Duplex+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+4G)+5G) | Required for 4G/5G. Use [FDD](https://www.google.com/search?q=FDD+Frequency+Division+Duplex+LTE) for 2G/3G. |
| Prediction model | — | [Path loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation+dB) model for this cell |
| Antenna | — | [Antenna pattern](https://www.google.com/search?q=antenna+radiation+pattern+file+format+MSI) from library |
| Site ID | — | Parent site reference |

**Color index:** Controls cell visualization color (None=blue, 1=red, 2=light green, 3=dark green, 4=light blue, 5=dark blue, 6=purple).

### Repeater

A signal [repeater](https://www.google.com/search?q=radio+repeater+signal+booster+telecom)/booster.

**Required:** Name, X, Y, [Azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north)

**Optional:** Height, Downtilt, [Electrical tilt](https://www.google.com/search?q=electrical+tilt+antenna+RET), Frequency (MHz), Power thresholds (1-2-3) and corresponding Power values (dBm), Misc loss, [Bandwidth](https://www.google.com/search?q=channel+bandwidth+radio+frequency+MHz), [Subcarrier spacing](https://www.google.com/search?q=[subcarrier](https://www.google.com/search?q=subcarrier+spacing+OFDM+LTE+5G)+spacing+OFDM+LTE+5G+kHz), Tx/[Rx MIMO](https://www.google.com/search?q=Rx+MIMO+receive+antenna+configuration), Technology, Prediction model, Antenna

### Radar

**Required:** Name, X, Y

**Optional:** Height (m), Downtilt, Frequency (MHz), Power (dBm), Misc Loss (dB), View Angle (vertical field of view in degrees), Prediction model

### CPE (Customer Premises Equipment)

**Required:** Name, X, Y

**Optional:** Height, Azimuth, Antenna, Power (dBm), Misc loss (dB), Cell ID (parent cell), [Throughput](https://www.google.com/search?q=network+throughput+downlink+uplink+[capacity](https://www.google.com/search?q=network+capacity+planning+telecom)) ([Mb/s](https://www.google.com/search?q=Mb+s+megabits+per+second+throughput)), Status, Notes

### Measurements

Drive-test or field measurement points.

**Required:** Field strength (dB), X, Y, Cell ID (binds measurement to a cell)

### Siren

Sound prediction source.

**Required:** Name, X, Y, Azimuth

**Optional:** Height (m), Downtilt, Frequency (MHz), Power (dBm), Misc loss (dB)

> ⚠️ Prediction model: **[ISO9613](https://www.google.com/search?q=ISO+9613+acoustic+propagation+standard) only** can be applied for sound loss calculations.

### Light

[Lighting](https://www.google.com/search?q=lighting+design+[lux](https://www.google.com/search?q=lux+light+intensity+measurement+unit)+calculation+photometry) point source for [lux](https://www.google.com/search?q=lux+light+intensity+measurement+unit) calculations.

**Required:** Name, X, Y, Azimuth

**Optional:** Height (m), Downtilt, Antenna (light pattern)

### Mesh Node

Node in a wireless [mesh network](https://www.google.com/search?q=mesh+network+wireless+topology).

**Required:** Name, X, Y

**Optional:** Height (m), Frequency (MHz), Power (dBm), Misc Loss (dB), Prediction model, Antenna, [Sensitivity](https://www.google.com/search?q=receiver+sensitivity+dBm+radio), Max connections, Layer (priority), Group name, Status, Type

---

## Selecting Objects

Selection modes:

| Mode | How to Use |
|------|-----------|
| **Rectangle** | Click once → move mouse → click again to define area |
| **Single click** | Click directly on an object |
| **Radius** | Set distance → click map → selects all objects within radius |
| **Polygon** | Click vertices → double-click to close and select |
| **Polygon layer** | Choose a polygon layer → click on map → selects objects within polygon |

Selected objects are highlighted on the map and listed in the Features panel.

**Controls:**
- **Clear selection** — deselects all
- **Search** — filter the selected objects list
- **Show in table** — open the attribute table for selected objects
- **Show only selected features** — hide non-selected objects in the list

---

## Editing Objects

Hover over any object in the Features list → click to open the edit dialog on the right.

- **Accept** — saves all changes
- **Cancel** — discards changes

Hover over a feature item for quick actions:
- **View from perspective** — viewpoint from the cell's position
- **Highlight feature** — highlight on map
- **Duplicate feature** — create a copy
- **Delete feature** — remove from map and database

---

## Move / Duplicate / Delete / Publish Selected

Select objects on the map, then:

- **Move** — drag selected objects to new location → Accept to save
- **Duplicate** — copy objects, optionally to another [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase) → Accept to save
- **Delete** — removes from map and database → Accept to confirm
- **[Publish](https://www.google.com/search?q=publish+layer+[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+Portal+web+map)** — [publish](https://www.google.com/search?q=publish+layer+ArcGIS+Portal+web+map) selected features as an [ArcGIS Portal](https://www.google.com/search?q=ArcGIS+platform)+Portal+enterprise+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)) [feature layer](https://www.google.com/search?q=ArcGIS+feature+layer+web+GIS) (select sharing: organization/public/groups)

---

## Related Topics

- [Network Object Requirements →](#network-object-requirements)
- [Importing Data (Training) →](#training-import-data)
- [RF Prediction →](#ce-express-rf-prediction)
- [Antenna Library →](#ce-express-antennas)
