# Features — Network Objects

> **Version:** CE Express v7.3

The **Features** tool is used to import, add, select, and edit all network objects on the map. Click the **Features** button in the left toolbar to open the tool.

---

## Object Types

CE Express supports the following network object types:

| Type | Description |
|------|-------------|
| **Site** | A physical location (tower, rooftop, pole) that hosts one or more cells |
| **Candidate Site** | A potential site location under evaluation |
| **Site Search Area** | A polygon or circle area defining where to search for candidate sites |
| **Cell** | A single radio sector — one antenna with defined position, direction, frequency, and power |
| **Repeater** | A signal booster that receives and retransmits a cell's signal |
| **Radar** | A radar object for radar prediction calculations |
| **CPE** | Customer Premises Equipment — a fixed receiver point bound to a specific cell |
| **Field Strength Measurement** | A measured signal level point, bound to a cell for model tuning |
| **Omen** | A generic point object for custom use cases |
| **Siren** | A sound-emitting object used in sound propagation calculations |
| **Light** | A light-emitting object used in optical propagation calculations |
| **Mesh Node** | A node in a mesh network for connectivity calculations |

---

## Site Parameters

### Required
| Attribute | Description |
|-----------|-------------|
| `site_name` | Site identification |
| `x` | Coordinate in the projected coordinate system |
| `y` | Coordinate in the projected coordinate system |

### Optional
| Attribute | Description |
|-----------|-------------|
| `height` | Height above the terrain |
| `city` | City where the site is located |
| `street` | Street address |
| `status` | Free-form status text |
| `type` | Free-form type text |
| `notes` | Free-form notes |

---

## Cell Parameters

### Required
| Attribute | Description |
|-----------|-------------|
| `cell_name` | Cell identification |
| `x` | Coordinate in the projected coordinate system |
| `y` | Coordinate in the projected coordinate system |
| `azimuth` | Cell direction from North in degrees (0–360) |

### Optional
| Attribute | Description |
|-----------|-------------|
| `site_name` | Parent site name |
| `height` | Antenna height above terrain in metres |
| `downtilt` | Mechanical tilt value in degrees |
| `frequency` | Frequency value in MHz |
| `power` | Power value in dBm |
| `misc_loss` | Miscellaneous loss value in dB |
| `antenna` | Antenna pattern name |
| `technology` | Network technology: `2G`, `3G`, `4G`, or `5G` |
| `prediction_model` | Prediction model for path loss simulation |
| `cell_load` | Cell load — affects RSSI, RSRQ, and DL Throughput calculations |
| `color_index` | Cell colour on the map (None=blue, 1=red, 2=light green, 3=dark green, 4=light blue, 5=dark blue, 6=purple) |

---

## Repeater Parameters

### Required
| Attribute | Description |
|-----------|-------------|
| `repeater_name` | Repeater identification |
| `x` | Coordinate in the projected coordinate system |
| `y` | Coordinate in the projected coordinate system |
| `azimuth` | Direction from North in degrees |

### Optional
| Attribute | Description |
|-----------|-------------|
| `height` | Height above terrain |
| `downtilt` | Mechanical tilt value |
| `frequency` | Frequency value in MHz |
| `power` | Power value in dBm |
| `misc_loss` | Miscellaneous loss value in dB |
| `antenna` | Antenna pattern name |

---

## Radar Parameters

### Required
| Attribute | Description |
|-----------|-------------|
| `radar_name` | Radar identification |
| `x` | Coordinate in the projected coordinate system |
| `y` | Coordinate in the projected coordinate system |

### Optional
| Attribute | Description |
|-----------|-------------|
| `height` | Height above terrain |
| `downtilt` | Mechanical tilt value |
| `frequency` | Frequency value in MHz |
| `power` | Power value in dBm |
| `misc_loss` | Miscellaneous loss value in dB |
| `view_angle` | Visible field (vertical angle) of the radar in degrees |
| `prediction_model` | Prediction model for path loss simulation |

---

## CPE Parameters

### Required
| Attribute | Description |
|-----------|-------------|
| `cpe_name` | CPE identification |
| `x` | Coordinate in the projected coordinate system |
| `y` | Coordinate in the projected coordinate system |

### Optional
| Attribute | Description |
|-----------|-------------|
| `height` | Height above terrain |
| `azimuth` | Direction from North in degrees |
| `antenna` | Antenna pattern name |
| `power` | Power value in dBm |
| `misc_loss` | Miscellaneous loss value in dB |
| `cell_id` | Binds the CPE to a specific cell |
| `throughput` | Data transfer speed in Mb/s |
| `status` | Current status |

---

## Importing Features

Use the **Import** option in the Features tool to bulk-load objects from a CSV or KMZ file.

If your import file uses different field names or units, enable **Use mapping** to match source columns to CE Express database fields. Mapping configurations can be saved as **mapping presets** for reuse.

---

## Editing Features

Click on any object in the Features tool list to open its attribute editor. Make changes and press **Accept** to save. To delete objects, select them on the map and press **Delete**, then confirm with **Accept**.
