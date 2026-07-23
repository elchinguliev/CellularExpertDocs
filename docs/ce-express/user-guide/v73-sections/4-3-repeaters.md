# 4.3 Repeaters

**repeater_name**
Object identification.

**Y**
Decimal degrees Y type coordinate in the WGS 1984 geographical coordinate system.

**X**
Decimal degrees X type coordinate in the WGS 1984 geographical coordinate system.

**height**
Repeater height above the ground in meters.

**azimuth**
Cell direction from the North in degrees.

**tilt**
Mechanical tilt value, negative numbers tilt up.

**frequency**
Frequency value in MHz.

**threshold 1-3**
The minimum field strength in dB at repeater location at which power of the corresponding index (1-3) will
be applied. Values should be in ascending order. If a higher threshold is satisfied, the power corresponding
to it will be used.

**power 1-3**
Power value in dBm.

**misc_loss**
Miscellaneous loss value in dB. Value is optional.

**bandwith**
Value in MHz. Required for 4G and 5G technologies. For other technologies define the value as 0.015.

**subcarrier_spacing**
Value in kHz. Required for 4G and 5G technologies. For other technologies define value 15.

**tx_mimo**
Transmitter antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64.

**rx_mimo**
Receiver antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64.

**technology**
Describes cell technology. Possible values are 2G, 3G, 4G, and 5G.

**prediction_model_id**
Sets the model type to be used:
- Value 1 – ITU R. P452
- Value 2 – UniMacro

**prediction_model_configuration_id**
Defines the prediction model configuration to be used in the model table. The objectID value is taken from
the prediction model table.

**frequency_group**
Used to divide calculations into parts. If the selection range includes two or more different frequency group
values, the cells won't be predicted together.

**antenna_id**
Describes the antenna ID from the antennas table. The objectID is used.

**workspace_id**
ID for the workspace. The field value is used to filter objects based on a chosen workspace. The parameter
is filled automatically.

**electrical_tilt**
Electrical tilt value, negative numbers tilt up
