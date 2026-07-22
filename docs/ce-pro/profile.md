# Profile

> **Note:** Shared across all CE Desktop Pro modules.

## 8. Profile

### 8.1 Profile Tool
A Profile in wireless communication represents the geographical and environmental characteristics of
the path between a transmitter and a receiver. It includes detailed information such as elevation data,
terrain heights, and any obstacles (e.g., buildings, trees, or mountains) that might impact signal
propagation.
All relevant calculations are already performed within the system. These include the power budget,
which factors in the total power available for transmission and reception while accounting for system
gains and losses, and the path loss, which measures the reduction in signal strength due to distance,
frequency, and environmental obstructions. The profile also provides the calculated angles, including
the elevation angle (vertical angle between the transmitter and receiver) and the azimuth angle
(horizontal direction). Additionally, it determines whether a direct line-of-sight exists between the two

![Image p141](../assets/images/ce-pro/rcp-guide/p141-img1.png)

![Image p141](../assets/images/ce-pro/rcp-guide/p141-img2.png)
points.
This comprehensive information is ready for use, enabling users to assess the feasibility and
performance of a communication link for network planning, optimization, and troubleshooting.
Click the button to open the Profile dialogue.
Profile tool enables you to determine the obstructions, elevation, and Fresnel zones between two points
on a map.

#### 8.1.1 Properties
Profile: Profile Selection

Profile selection allows for quick switching between profiles while retaining the most recently defined

![Image p142](../assets/images/ce-pro/rcp-guide/p142-img1.png)

![Image p142](../assets/images/ce-pro/rcp-guide/p142-img2.png)
parameters. This feature is especially useful for comparing and verifying calculations across different
Tx and Rx configurations. When a new profile is created, it is automatically assigned a name and
appears in the Profile Selection option.
Profile can be saved or removed from the list.
| Parameter | Description |
|---|---|
| Save | The option saves the profile to Docs Manager tool with all defined parameters. |
| Close | Removes profile from the list in Profile Selection. |
| Close All | Removes all profiles from Profile Selection list. |
Profile: General
Fresnel Minimal Clearance, %
Percentage by which the primary Fresnel zones will be scaled up or down thus creating a secondary
Fresnel zone. The percentage must be in the range of 1 to 200. The value can be changed either by
inputting it manually or by using the slider.
Transmitter Template
The template that is used for transmitter’s default values.
Receiver Template
The template that is used for receiver’s default values.

| Parameter | Description |
|---|---|
| Profile: Transmitter | Toggling the switch to the left of Transmitter will enable the Fixed Transmitter functionality, which will modify only the receiver’s positioning when drawing the profile on the map. |
| Cell | A cell from which the profile will be drawn. The parameters of the cell will be taken into calculation if the cell is snapped to by the profile tool. |
| Latitude | Decimal degrees Y type coordinate. |
| Longitude | Decimal degrees X type coordinate. |
| Height, m | Height above the ground in meters. The minimum value must be 1m. |
Azimuth towards receiver
Enabled by default. When enabled, the transmitter’s azimuth is towards the receiver. Disabling this
option it would take azimuth value from the Cell object, and use it for FWA Power Budget calculations,
it also allows the user to enter a custom azimuth value for the transmitter.
Downtilt towards receiver
Enabled by default. When enabled, the transmitter’s tilt is towards the receiver. Disabling this option it
would take tilt value from the Cell object, and use it for FWA Power Budget calculations, it allows the
user to enter a custom tilt value for the transmitter.
El. Downtilt, deg.
Electrical downtilt value for the transmitter, in degrees.

The antenna for the transmitter can be selected from the table below the El. Downtilt, deg input. Its

![Image p144](../assets/images/ce-pro/rcp-guide/p144-img1.png)
pattern can be viewed by clicking the View Antenna button on the right side.
Frequency of the transmitter.
| Parameter | Description |
|---|---|
| Bandwidth, MHz | Bandwidth of the transmitter. |
| Power, dBm | A power that the transmitter possesses. |
| Misc Loss, dB | Miscellaneous loss value in dB. Value is not required. |
| Tx mimo | Transmitter antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64. |
| Rx mimo | Receiver antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64. |
| Subcarrier spacing | Value in kHz. |

Profile: Receiver
| Parameter | Description |
|---|---|
| Latitude | Decimal degrees Y type coordinate. |
| Longitude | Decimal degrees X type coordinate. |
| Height, m | Height above the ground in meters. The minimum value must be 1m. |
| Azimuth towards transmitter | Enabled by default. When enabled, the receiver’s azimuth is towards the transmitter. Disabling this option it would take azimuth value from the receiver (Cell) object, and use it for FWA Power Budget |

calculations, it also allows the user to enter a custom azimuth value for the receiver.
Downtilt towards transmitter
Enabled by default. When enabled, the receiver’s tilt is towards the transmitter. Disabling this option it

![Image p146](../assets/images/ce-pro/rcp-guide/p146-img1.png)
would take tilt value from the receiver (Cell) object, and use it for FWA Power Budget calculations,
it allows the user to enter a custom tilt value for the receiver.
Power, dBm
A power that the receiver possesses.
Misc Loss, dB
Miscellaneous loss value in dB. Value is not required.
Profile: Prediction Model
Double-click the prediction model from the list to select it for the profile.

#### 8.1.2 Draw Profile
When the Profile tool is selected and enabled, you will be able to select two points on the map in turn
creating a Profile line.
The profile also lets you snap to different Cellular Expert network objects. If the object to which the
user snaps is a cell, all parameters of that cell that are necessary to draw a profile will be read and
included in the calculations. If the object is not a cell, then only the name and the object’s
coordinates will be taken.
Most of these values will be displayed in the Profile pane shown above. If you change the values in the
pane, these changes will be reflected in the Profile plot by redrawing it.
Upon the selection of a second point, these geometries will be created between the points:
• LOS (green) - the distance until the first obstruction in the profile’s way
• OLOS (orange) – the distance until the first clutter LOS obstruction
• NLOS (red) – the obstructed path between the sender and receiver
• Lowest Clearance (yellow) – the point at which NLOS has the lowest clearance to the obstacle
• Rx (purple) – the receiver point
• Tx (green) – the transmitter point
• Fresnel (blue) – the Fresnel lines

The Profile plot illustrating these geometries, obstacles (buildings), and the Fresnel zone will appear in

![Image p147](../assets/images/ce-pro/rcp-guide/p147-img1.png)

![Image p147](../assets/images/ce-pro/rcp-guide/p147-img2.png)

![Image p147](../assets/images/ce-pro/rcp-guide/p147-img3.png)
a dockpane below. You can inspect the values at particular points by moving the cursor around the
plot. The cursor movement on the plot will be projected as a moving point on the map. If a cell is
selected for the transmitter, the cell’s tilt (the sum of mechanical and electrical tilts) and vertical
beamwidth are displayed as additional symbols: a light blue line and a darker blue cone
respectively. The length of the cell tilt and antenna vertical beamwidth symbols is the radius of the
prediction model selected for the cell.
The button allows you to see the Prediction Calculation results.

You can change the colors of the profile by clicking the colored squares near the names of the parameters.

![Image p148](../assets/images/ce-pro/rcp-guide/p148-img1.png)

![Image p148](../assets/images/ce-pro/rcp-guide/p148-img2.png)
The colors will be updated automatically. You can toggle the visibility of each separate parameter of
the profile by clicking on the name of the element. Enabled elements are indicated by bold text,
and disabled elements are indicated by regular text.

You can change the height of the transmitter/receiver points by dragging their ends on the plot.
Hovering the cursor over the plot displays a tooltip with the meter values for profile, building, clutter,

![Image p149](../assets/images/ce-pro/rcp-guide/p149-img1.png)

![Image p149](../assets/images/ce-pro/rcp-guide/p149-img2.png)
elevation, distance, etc., as well as their representations in colors.

8.1.2.1 Adjust Data
Adjust data is found on the Profile Plot dockpane near the Results. The tool lets you change the

![Image p150](../assets/images/ce-pro/rcp-guide/p150-img1.png)

![Image p150](../assets/images/ce-pro/rcp-guide/p150-img2.png)
elevation, building, and clutter data of the area visible in the profile plot.
When the Adjust tab is opened, select a desirable range for the data adjustment on the plot.

You can make slight changes to the range of the selection area by hovering over the area's edges and

![Image p151](../assets/images/ce-pro/rcp-guide/p151-img1.png)

![Image p151](../assets/images/ce-pro/rcp-guide/p151-img2.png)

![Image p151](../assets/images/ce-pro/rcp-guide/p151-img3.png)

![Image p151](../assets/images/ce-pro/rcp-guide/p151-img4.png)
dragging them. To adjust the values, click on one of the text boxes and insert the value.
To change multiple values simultaneously, drag across the adjustment table and select multiple rows.
Changing the value of a single text box will also change all the other chosen rows’ values in that
text box. The selected area will be highlighted on the profile plot.
To update the values, either select an unselected row or press the button.

To reset the adjusted values to defaults, click the Refresh button .
Manual Profile
If you want to insert specific coordinates and draw a profile that way, you can insert these values in the

![Image p152](../assets/images/ce-pro/rcp-guide/p152-img1.png)

![Image p152](../assets/images/ce-pro/rcp-guide/p152-img2.png)

![Image p152](../assets/images/ce-pro/rcp-guide/p152-img3.png)

![Image p152](../assets/images/ce-pro/rcp-guide/p152-img4.png)
Profile pane and click the Manual Profile button.
Dynamic Profile
The button toggles the Dynamic Profile.
Dynamic Profile lets you see Profile calculations and the plot be drawn in real-time as the cursor
moves. Whenever the cursor stops momentarily – the profile gets drawn. The transmitter point
needs to be entered for the dynamic profile to be activated. The previous transmitter point will be
chosen if the point is not currently entered.
If a second point is selected while the profile is being drawn, the dynamic profile will be disabled, and
the LOS lines will appear on the map.

#### 8.1.3 Tools
Reflections are considered in profile and RF calculations to assess how radio waves bounce off
surfaces, affecting signal path and strength.
To enable reflections select either Single or Multipath Reflection. Be aware that if reflections are not
visible you may need to adjust the height of the receiver/transmitter accordingly.
It is recommended to disable the Step Plot of the profile before using Reflections (see Settings).
Use Single Reflection
Enable a reflection that will reflect straight from the transmitter to the receiver point with the smallest

![Image p153](../assets/images/ce-pro/rcp-guide/p153-img1.png)

![Image p153](../assets/images/ce-pro/rcp-guide/p153-img2.png)
angle.

| Parameter | Description |
|---|---|
| Use Multipath Reflections | Enable all reflections that happen along the profile line. |
| Use Divergence Factor | Quantifies the extent to which a reflected signal spreads out, affecting its strength and coverage. |
| Step Size | The length period by which the reflection will be calculated. The step size is determined by taking the average cell size of the elevation raster. |
| Polarizations | The polarization of reflections (vertical or horizontal). |
| Use Clutter Classes | Enables the use of default clutter classes for the reflection calculations (see Clutter Classes ). If disabled, custom values may be used for conductivity and permittivity. |
Select Reflection Range
Lets you set a range in which the reflection calculations should happen. This will affect both Single and

![Image p154](../assets/images/ce-pro/rcp-guide/p154-img1.png)

![Image p154](../assets/images/ce-pro/rcp-guide/p154-img2.png)
Multipath reflections and help highlight specific important areas along the profile as well as speed
up the calculation process.
The range will be enabled as soon as a profile is drawn.
You can select this range on the plot, by holding down the left mouse button and dragging across the
screen.
Reflection results will appear in the Profile Results table.

8.1.3.1 Reflection Analysis
The Reflection Analysis tool for Profile is designed to help analyze and visualize signal reflections based

![Image p155](../assets/images/ce-pro/rcp-guide/p155-img1.png)
on the changes in various profile parameters like frequency, transmitter height, receiver height, and K-
factor. Reflections must be enabled to perform analysis, and the Single Reflection option is automatically
enabled when the tool is selected.

| Parameter | Description |
|---|---|
| Dependency on Frequency | Calculate reflection analysis based on frequency range (from GHz to GHz) |
| Dependency on Receiver height | Calculate reflection analysis based on receiver height range (from m to m) |
| Dependency on Transmitter height | Calculate reflection analysis based on transmitter height range (from m to m) |
| Dependency on K-Factor | Calculate reflection analysis based on K-factor range (from radius, km to radius, km) |

![Image p156](../assets/images/ce-pro/rcp-guide/p156-img1.png)

The reflection analysis results for each type of dependency are displayed in the Reflection Analysis tab
of the Calculated Profile window.

#### 8.1.4 Import
Import a profile by selecting a profile file in the Import section. Supported formats: .pl2 (path loss file).

![Image p157](../assets/images/ce-pro/rcp-guide/p157-img1.png)

![Image p157](../assets/images/ce-pro/rcp-guide/p157-img2.png)
Once imported successfully, the profile data may then be customized.

Load Profile
Creates the profile with the provided data.

#### 8.1.5 Export (Profile Report)
The input data and calculation results can be automatically transferred into a Profile Report. This report
will show transmitter/receiver input data, calculation results as well as the Profile plot and map view in which

![Image p158](../assets/images/ce-pro/rcp-guide/p158-img1.png)

![Image p158](../assets/images/ce-pro/rcp-guide/p158-img2.png)
the profile was drawn. The report can be exported in PDF and PL2 formats.

The resulting Profile report will look similar to this example:

![Image p159](../assets/images/ce-pro/rcp-guide/p159-img1.png)

#### 8.1.6 Settings
Currently, you can configure the profile’s visual properties and controls in profile settings. The settings

![Image p160](../assets/images/ce-pro/rcp-guide/p160-img1.png)
can be changed once a profile is drawn.
| Parameter | Description |
|---|---|
| Show Step Plot | Display data points as a series of steps rather than a smooth line or individual points. |
| Transmitter height change stepnter | The step (in meters) for changing the transmitter height when dragging it in the Profile graph. The default value is 0.5 meters. |
| Receiver height change step | The step (in meters) for changing the receiver height when dragging it in the Profile graph. The default value is 0.5 meters. |
value is 0.5 meters.
