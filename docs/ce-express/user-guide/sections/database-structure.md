# Database Structure



## 4.1 Sites

Describes the tower's location and its identification. An object is not used for the calculations. It is possible

![Image p261](../../../assets/images/ce-express/user-guide-v73/p261-img1.png)

![Image p261](../../../assets/images/ce-express/user-guide-v73/p261-img2.png)

![Image p261](../../../assets/images/ce-express/user-guide-v73/p261-img3.png)
to add additional fields, but here are the main fields used for this object.
site_name
Object identification.

| Parameter | Description |
|---|---|
| Y | Decimal degrees Y type coordinate in the WGS 1984 geographical coordinate system. |
| X | Decimal degrees X type coordinate in the WGS 1984 geographical coordinate system. |
| workspace_id | ID for the workspace. This field value is used to filter objects based on a chosen workspace. The parameter is filled automatically. |
| height | Height of the site in meters. |

## 4.2 Cells

| cell_name | Object identification. |
| Y | Decimal degrees Y type coordinate in the WGS 1984 geographical coordinate system. |
| X | Decimal degrees type coordinate in the WGS 1984 geographical coordinate system. |
| height | Cell height above the ground in meters. |
| azimuth | Cell direction from the North in degrees. |
| tilt | Mechanical tilt value , negative numbers tilt up. |
| frequency | Frequency value in MHz. |
| power | Power value in dBm. |
| misc_loss | Miscellaneous loss value in dB. |
bandwidth

Value in MHz. Required for 4G and 5G technologies. For other technologies define the value as 0.015.
| Parameter | Description |
|---|---|
| noise_figure | Value in dB. Required for 4G and 5G technologies. |
| downlink_duplex_factor | Value range from 0 to 1. Required for 4G and 5G technologies, and used for Downlink Throughput calculations. |
| subcarrier_spacing | Value in kHz. Required for 4G and 5G technologies. For other technologies define value 15. |
| tx_mimo | Transmitter antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64. |
| rx_mimo | Receiver antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64. |
active_antenna_effect
This parameter is dedicated to smart antenna modelling. The default value is 0, but if massive MIMO is
used, a smart antenna effect can be included to lower the interference and boost the throughput.
Recommended values:
- For MIMO 32x32 – value 6.
- For MIMO 64x64 – value 9.
cell_load
This parameter is described in percentage and varies from 0 to 100. It describes the load of a cell. The cell
load affects RSSI, RSRQ, DL Throughput calculations. For example, if the cell load is higher, the DL
Throughput is lower.
workspace_id
ID for the workspace. The field value is used to filter objects based on a chosen workspace. The parameter
is filled automatically.
color_index
Describes the cell visualization. Available values:
- None – blue color.
- 1 – red color.
- 2 – light green color.
- 3 – dark green color.
- 4 – light blue color.
- 5 – dark blue color.
- 6 – purple color.
technology
Describes the cell technology. Possible values are 2G, 3G, 4G, and 5G.
prediction_model_configuration_id
Defines the prediction model configuration to be used in the model table. The objectID value is taken from
the prediction model table.

frequency_group
Used to divide calculations into parts. If the selection range includes two or more different frequency group
values, the cells won’t be predicted together.
antenna_id
Describes the antenna ID from the antennas table. The objectID is used.
carriers
Describes the carrier values used for 2G calculations: C/I interference and C/A interference. The values
are written in brackets, […]. If more than one value is defined, the values are separated by a comma. If
there is no carrier information, the brackets are left empty [].
| Parameter | Description |
|---|---|
| site_id | Site identification. This field value is optional. |
| duplex_mode | Lets the user select what type of duplexing technique he wants to assign to the cell. |
| electrical_tilt | Electrical tilt value, negative numbers tilt up |
| status | free-form text. |
| type | free-form text. |

## 4.3 Repeaters

| repeater_name | Object identification. |
| Y | Decimal degrees Y type coordinate in the WGS 1984 geographical coordinate system. |
| X | Decimal degrees X type coordinate in the WGS 1984 geographical coordinate system. |
| height | Repeater height above the ground in meters. |
| azimuth | Cell direction from the North in degrees. |
| tilt | Mechanical tilt value, negative numbers tilt up. |
| frequency | Frequency value in MHz. |

threshold 1-3
The minimum field strength in dB at repeater location at which power of the corresponding index (1-3) will
be applied. Values should be in ascending order. If a higher threshold is satisfied, the power corresponding
to it will be used.
| Parameter | Description |
|---|---|
| power 1-3 | Power value in dBm. |
| misc_loss | Miscellaneous loss value in dB. Value is optional. |
| bandwith | Value in MHz. Required for 4G and 5G technologies. For other technologies define the value as 0.015. |
| subcarrier_spacing | Value in kHz. Required for 4G and 5G technologies. For other technologies define value 15. |
| tx_mimo | Transmitter antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64. |
| rx_mimo | Receiver antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64. |
| technology | Describes cell technology. Possible values are 2G, 3G, 4G, and 5G. |
| prediction_model_id | Sets the model type to be used: Value 1 – ITU R. P452 • Value 2 – UniMacro • |
| prediction_model_configuration_id | Defines the prediction model configuration to be used in the model table. The objectID value is taken from the prediction model table. |
| frequency_group | Used to divide calculations into parts. If the selection range includes two or more different frequency group values, the cells won’t be predicted together. |
| antenna_id | Describes the antenna ID from the antennas table. The objectID is used. |
| workspace_id | ID for the workspace. The field value is used to filter objects based on a chosen workspace. The parameter is filled automatically. |
| electrical_tilt | Electrical tilt value, negative numbers tilt up |

## 4.4 Radars

| Parameter | Description |
|---|---|
| Radar_name | Object identification. |
| Y | Decimal degrees Y type coordinate in the WGS 1984 geographical coordinate system. |
| X | Decimal degrees X type coordinate in the WGS 1984 geographical coordinate system. |
| Height | Radar height above the ground in meters |
| Tilt | Mechanical tilt value, negative numbers tilt up. |
| Frequency | Frequency value in MHz. |
| Power | Power value in dBm. Value is optional. |
| Misc_loss | Miscellaneous loss value in dB. Value is optional. |
| View_angle | Radar radiation vertical height in degrees centered at the tilt value. |
| Prediction_model_id | Sets the model type to be used: Value 1 – ITU R. P452 • • Value 2 – UniMacro |
| Prediction_model_configuration_id | Defines the prediction model configuration to be used in the model table. The objectID value is taken from the prediction model table. |
| Workspace_id | ID for the workspace. The field value is used to filter objects based on a chosen workspace. The parameter is filled automatically. |

## 4.5 CPE

| Cpe_name | Object identification. |
| Y | Decimal degrees Y type coordinate in the WGS 1984 geographical coordinate system. |
X

Decimal degrees X type coordinate in the WGS 1984 geographical coordinate system.
| Parameter | Description |
|---|---|
| Height | CPE height above the ground in meters |
| Azimuth | Cell direction from the North in degrees. |
| Antenna_id | Describes the antenna ID from the antennas table. The objectID is used. |
| Cell_id | Cell identification. |
| Throughput | Throughput sold to customer (used in network availability calculation) |
| Power | Power value in dBm. |
| Misc_loss | Miscellaneous loss value in dB. |
| Status | free-form text. |
| Notes | free-form text. |
| Workspace_id | ID for the workspace. The field value is used to filter objects based on a chosen workspace. The parameter is filled automatically. |

## 4.6 Measurements

| Fs | Measured field strength. |
| Y | Decimal degrees Y type coordinate in the WGS 1984 geographical coordinate system. |
| X | Decimal degrees X type coordinate in the WGS 1984 geographical coordinate system. |
| Cell_id | Cell identification. |
| Workspace_id | ID for the workspace. The field value is used to filter objects based on a chosen workspace. The parameter is filled automatically. |
is filled automatically.

## 4.7 Workspace

| Parameter | Description |
|---|---|
| Workspace_name | Workspace identification. |
| Extent_xmin | Minimum workspace extent longitude |
| Extent_ymin | Minimum workspace extent latitude |
| Extent_xmax | Maximum workspace extent longitude |
| Extent_ymax | Maximum workspace extent latitude |
| Extra_layers | JSON array containing links to ArcGIS layer services. e.g.: [“url1”, “url2”] |
| Use_clutter_loss | Possible values: • t – clutter losses included in the prediction model. f – clutter losses not included in the prediction model. • |
| Calculate_eirp | True – EIRP is calculated with the formula power - misc_loss + antenna gain. False – power value is used as EIRP. |
| Geodata_set_id | Path to folder containing geodata rasters: elevation.tif, building_height.tif (optional), clutter_classes.tif (optional), clutter_height.tif (optional). |
