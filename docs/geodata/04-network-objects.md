---
id: network-object-requirements
title: Network Object Requirements
product: Both
category: Geodata
order: 4
related:
  - ce-express-features
  - geodata-requirements
---

# Requirements for CE Network Objects

CE [network objects]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=radio+network+objects+sites+cells+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)) must meet minimum field requirements for successful [import]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=data+import+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) and use in calculations.

## Primary Data Structure

### Import from CSV File

- First row: **field names** (column headers)
- Subsequent rows: values
- Field names are **not case-sensitive** — CE includes a mapping function to align external names with CE database fields

### Import from __S7__+platform)+Portal+enterprise+web+GIS)

- Point layer shared on [ArcGIS Enterprise](https://www.google.com/search?q=ArcGIS+Enterprise+server+GIS) Portal or [ArcGIS Online](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+Online+cloud+GIS+platform)
- CE imports via Portal Item ID
- [Field mapping](https://www.google.com/search?q=field+mapping+data+[import](https://www.google.com/search?q=data+import+GIS+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format))+GIS) is handled automatically via the CE mapping function

---

## Cells (Sectors)

### Minimum Requirements

| CE Field | Unit | Example | Description |
|----------|------|---------|-------------|
| `y` (Latitude) | Decimal degrees | 49.9993 | Y coordinate in [WGS84](https://www.google.com/search?q=WGS84+geographic+coordinate+system) (for initial CSV import) |
| `x` (Longitude) | Decimal degrees | 33.6573 | X coordinate in [WGS84](https://www.google.com/search?q=WGS84+World+Geodetic+System+coordinate) |
| `cell_` ([Cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) ID) | — | ABC_001 | Unique [cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) identifier |

### Optional Fields

| Field | Unit | Notes |
|-------|------|-------|
| **Height** | m [AGL](https://www.google.com/search?q=AGL+Above+Ground+Level+height+measurement) | Antenna [height above ground](https://www.google.com/search?q=height+above+ground+[AGL](https://www.google.com/search?q=AGL+Above+Ground+Level+height+measurement)+antenna) |
| **[Azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north)** | degrees | 0–360°, direction from North |
| **[Mechanical tilt](https://www.google.com/search?q=mechanical+tilt+antenna+[downtilt](https://www.google.com/search?q=antenna+downtilt+mechanical+electrical+degrees))** | degrees | Physical antenna [downtilt](https://www.google.com/search?q=antenna+downtilt+mechanical+electrical+degrees) |
| **[Electrical tilt](https://www.google.com/search?q=electrical+tilt+antenna+RET)** | degrees | Electronic beam tilt |
| **Frequency** | [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit) | [Carrier frequency](https://www.google.com/search?q=carrier+frequency+radio+transmission) |
| **Power** | [dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit) | [Transmit power](https://www.google.com/search?q=transmit+power+[dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit)+radio+antenna) |
| **[Antenna gain](https://www.google.com/search?q=antenna+gain+[dBi](https://www.google.com/search?q=dBi+decibel+isotropic+antenna+gain)+directional)** | [dBi](https://www.google.com/search?q=dBi+decibel+isotropic+antenna+gain) | Peak [antenna gain](https://www.google.com/search?q=antenna+gain+dBi+directional) |
| **Losses** | [dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit) | Cable, connector, combiner losses |
| **[Bandwidth](https://www.google.com/search?q=channel+bandwidth+radio+frequency+[MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit))** | MHz | Channel [bandwidth](https://www.google.com/search?q=channel+bandwidth+radio+frequency+MHz) (required for [4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)/[5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network)) |
| **[Subcarrier spacing](https://www.google.com/search?q=[subcarrier](https://www.google.com/search?q=subcarrier+spacing+[OFDM](https://www.google.com/search?q=OFDM+Orthogonal+Frequency+Division+Multiplexing)+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+[4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)+mobile)+[5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network))+spacing+[OFDM](https://www.google.com/search?q=OFDM+Orthogonal+Frequency+Division+Multiplexing)+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+4G+mobile)+5G+[kHz](https://www.google.com/search?q=kHz+kilohertz+frequency+unit))** | [kHz](https://www.google.com/search?q=kHz+kilohertz+frequency+unit) | SCS (required for 5G) |
| **[TX MIMO](https://www.google.com/search?q=Tx+[MIMO](https://www.google.com/search?q=MIMO+Multiple+Input+Multiple+Output+antenna+technology)+transmit+antenna+configuration)** | — | Transmit antenna count (1,2,4,8,16,32,64) |
| **[RX MIMO](https://www.google.com/search?q=Rx+[MIMO](https://www.google.com/search?q=MIMO+Multiple+Input+Multiple+Output+antenna+technology)+receive+antenna+configuration)** | — | Receive antenna count |
| **Technology** | — | [2G](https://www.google.com/search?q=2G+GSM+mobile+network+second+generation), [3G](https://www.google.com/search?q=3G+UMTS+HSPA+mobile+network), 4G, 5G, [NB-IoT](https://www.google.com/search?q=NB+IoT+Narrowband+cellular) |
| **Antenna name** | — | Must match antenna in CE library |
| **[Site](https://www.google.com/search?q=cell+site+tower+base+station+location) ID** | — | Parent [site](https://www.google.com/search?q=cell+site+tower+base+station+location) identifier (links cell to site) |
| **Duplex mode** | [FDD](https://www.google.com/search?q=FDD+Frequency+Division+Duplex+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+4G))/[TDD](https://www.google.com/search?q=TDD+Time+Division+Duplex+LTE+5G) | Required for 4G/5G |

---

## Sites (Towers)

Sites are optional — cells can exist without explicit site records. Sites add:

| Field | Description |
|-------|-------------|
| **Site name** | Unique identifier |
| **Latitude / Longitude** | [WGS84](https://www.google.com/search?q=WGS84+World+Geodetic+System+coordinate) decimal degrees |
| **Height** | Tower/mast height AGL (m) |
| **Type** | Monopole, Lattice, Rooftop, etc. |
| **Owner** | Network operator or tower company |
| **Address** | Physical address |

---

## Antenna Patterns

For each cell, an [antenna pattern](https://www.google.com/search?q=antenna+radiation+pattern+format) must be assigned from the CE antenna library.

### Antenna File Formats

| Format | Extension | Notes |
|--------|-----------|-------|
| [MSI Planet](https://www.google.com/search?q=MSI+Planet+antenna+pattern+format) | `.msi` | **Standard format — recommended** |
| Planet | `.pln` | Alternative format |

### Antenna File Requirements

An antenna file must include:
- **Horizontal pattern** (0–360° in 1° steps, [dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit) relative to peak)
- **Vertical pattern** (−180° to +180° in 1° steps, dB relative to peak)
- **Peak gain** (dBi)
- **Frequency** (MHz)
- **Manufacturer** and **model name** (for library identification)

---

## Minimum Viable CSV for Import

### Sites CSV

```csv
Name,Latitude,Longitude,Height
SITE_001,51.5074,-0.1278,30
SITE_002,51.5200,-0.1150,25
```

### Cells CSV

```csv
CellName,Latitude,Longitude,Azimuth,Height,Technology,Frequency
CELL_001A,51.5074,-0.1278,0,25,4G,1800
CELL_001B,51.5074,-0.1278,120,25,4G,1800
CELL_001C,51.5074,-0.1278,240,25,4G,1800
```

---

## Related Topics

- [Features Tool — Adding Objects →](#ce-express-features)
- [Importing Data →](#training-import-data)
- [Geodata Requirements →](#geodata-requirements)
