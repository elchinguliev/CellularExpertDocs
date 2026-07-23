# 3.1.16 Profile

Click this button ![icon](../../../assets/images/ce-express/user-guide-v73/p142-img1.png) to open [Profile tool](#kw:when-to-use-the-profile-tool:ce-express-profile).

This tool generates a detailed profile between two points. The locations From (transmitter) and To (receiver) can be chosen by clicking on the map. The first click defines the transmitter, the second one the receiver.

![Image p142](../../../assets/images/ce-express/user-guide-v73/p142-img2.png)

3.1.16.1 Properties

![Image p142](../../../assets/images/ce-express/user-guide-v73/p142-img3.png)

**Calculation settings**

**Reference Fresnel clearance**

Percentage by which the primary Fresnel zones will be scaled up or down thus creating a secondary Fresnel zone. The percentage must be in the range of 1 to 200 %.

**Lock transmitter location**

Toggling the switch will enable the Locked Transmitter location, which will modify only the receiver’s positioning when drawing the profile on the map.

**Prediction model**

Prediction model list.

**Transmitter template**

The template that is used for transmitter’s default values.

**Receiver template**

The template that is used for receiver’s default values.

![Image p143](../../../assets/images/ce-express/user-guide-v73/p143-img1.png)

**Transmitter**

**Snapped feature**

A feature from which the profile will be drawn. The parameters of the feature will be taken into calculation if the feature is snapped to by the [profile tool](#kw:when-to-use-the-profile-tool:ce-express-profile).

**X**

X coordinate of the transmitter.

**Y**

Y coordinate of the transmitter.

**Height**

Height above the ground in meters.

**Azimuth towards receiver**

Enabled by default. When enabled, the transmitter’s azimuth automatically set towards the receiver. Disabling this option allows the user to enter a static azimuth value for the transmitter.

**Downtilt towards receiver**

Enabled by default. When enabled, the transmitter’s tilt is automatically set towards the receiver. Disabling this option allows the user to enter a static tilt value for the transmitter.

**El. Downtilt**

Electrical downtilt value for the transmitter, in degrees.

**Antenna**

Antenna that will be used in the prediction calculations.

**Frequency**

The frequency value in MHz.

**Bandwidth**

Value in MHz. Required for 4G and 5G technologies. For other technologies define the value as 0.015.

**Power**

Transmitter power in dBm. If calculate EIRP is set to false in the workspace settings, the power value is assumed to be EIRP.

**Misc. loss**

Miscellaneous loss value in dB.

**TX MIMO**

Transmitter antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64.

**RX MIMO**

Receiver antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64.

**Subcarrier spacing**

Value in kHz. Required for 4G and 5G technologies. For other technologies define value 15.

![Image p145](../../../assets/images/ce-express/user-guide-v73/p145-img1.png)

**Receiver**

**X**

X coordinate of the receiver.

**Y**

Y coordinate of the receiver.

**Height**

Receiver height above the receiver reference height selected in the workspace settings.

**Azimuth towards transmitter**

Enabled by default. When enabled, the receiver’s azimuth automatically set towards the transmitter.

Disabling this option allows the user to enter a static azimuth value for the receiver.

**Downtilt towards transmitter**

Enabled by default. When enabled, the receiver’s tilt is automatically set towards the transmitter. Disabling this option allows the user to enter a static tilt value for the receiver.

**Antenna**

Antenna that will be used in the prediction calculations.

**Power**

A power that the receiver possesses.

**Misc. loss**

Miscellaneous loss value in dB.

3.1.16.2 Draw profile

When the [Profile tool](#kw:when-to-use-the-profile-tool:ce-express-profile) is selected you will be able to select two points on the map in turn creating a Profile line.

The profile also lets you snap to different [network objects](#kw:object-types:ce-express-network-objects) (cells, CPE, sites). To snap to an object, use the CTRL key and hover the mouse near the required feature. Snapped features appear in the Snapped feature dropdown list under transmitter and receiver sections. Once a snapped feature is selected in the dropdown menu, all parameters of that feature that are necessary to draw a profile will be read and included in the calculations.

The profile is automatically recalculated when a new parameter is defined.
Upon the selection of a second point, these geometries will be created between the points:
- LOS (green) - the section until the first obstruction in the profile’s way
- OLOS (yellow) – the section of profile that is obstructed by clutter
- NLOS (red) – the section of profile that is obstructed by buildings or earth
- Rx (purple) – the receiver point
- Tx (green) – the transmitter point
- Fresnel (blue) – the Fresnel lines

![Image p146](../../../assets/images/ce-express/user-guide-v73/p146-img1.png)

You can inspect the values at particular points by moving the cursor around the plot. The cursor movement on the plot will be projected as a moving point on the map.

![Image p147](../../../assets/images/ce-express/user-guide-v73/p147-img1.png)

Zoom in/out in the profile view.

![Image p147](../../../assets/images/ce-express/user-guide-v73/p147-img2.png)

Click on![Image p147](../../../assets/images/ce-express/user-guide-v73/p147-img3.png) button to view the see the Calculation results.

![Image p148](../../../assets/images/ce-express/user-guide-v73/p148-img1.png)

3.1.16.3 Profile report
The input data and calculation results can be automatically transferred into a Profile Report. This report will show transmitter/receiver input data, calculation results as well as the Profile plot and map view in which the profile was drawn.

![Image p148](../../../assets/images/ce-express/user-guide-v73/p148-img2.png)

The resulting Profile report will look similar to this example:

![Image p149](../../../assets/images/ce-express/user-guide-v73/p149-img1.png)
