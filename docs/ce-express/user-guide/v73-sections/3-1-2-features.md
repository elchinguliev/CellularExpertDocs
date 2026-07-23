# 3.1.2 Features

Click this button ![icon](../../../assets/images/ce-express/user-guide-v73/p018-img2.png) to open Features tool.

Use this tool to import or add features, select and visualize them.

3.1.2.1 Import

The widget allows the creation of objects from a text file. To start importing new objects press the Import features button.

![Image p19](../../../assets/images/ce-express/user-guide-v73/p019-img1.png)

Select the object type.

![Image p19](../../../assets/images/ce-express/user-guide-v73/p019-img2.png)

A new dialog on the right side of the window will appear. The widget imports object data to the database.
The imported objects will be displayed automatically on the map. The supported file formats are CSV and
KMZ.

To start the import process, select or drag and drop a CSV or KMZ file.
3.1.2.1.1 Mapping
The data in the import files may have names, values and units which do not match the data in the Cellular

![Image p20](../../../assets/images/ce-express/user-guide-v73/p020-img1.png)

![Image p20](../../../assets/images/ce-express/user-guide-v73/p020-img2.png)
Expert database. To resolve such issues, check Use mapping button.

Source - the name of the value that is written in the data file.
Fill - value which will be used when an object in the data file has no value for a particular property. In this

![Image p21](../../../assets/images/ce-express/user-guide-v73/p021-img1.png)
example, if “Azimuth” is not set, then it will by default be assigned the value of 0. Leaving the default to
empty means that no default value will be applied.

3.1.2.1.2 Mapping presets
It is possible to create import presets.
To create a preset, first define source or fill value, then press New mapping preset button.
A new preset will be created.
Define a preset name. The defined preset will be applied the next time for importing.
Apply
Applies a mapping preset for importing file.
Delete
Deletes a preset.
3.1.2.2 Add features

![Image p22](../../../assets/images/ce-express/user-guide-v73/p022-img1.png)

![Image p22](../../../assets/images/ce-express/user-guide-v73/p022-img2.png)

![Image p22](../../../assets/images/ce-express/user-guide-v73/p022-img3.png)

![Image p22](../../../assets/images/ce-express/user-guide-v73/p022-img4.png)

Select the object type.
A new dialog on the right side of the window will appear.
New objects can be created in several ways. They can be:
- Created from templates
- Created with Cellular Expert tools from zero (define all parameters in the process)

![Image p23](../../../assets/images/ce-express/user-guide-v73/p023-img1.png)

![Image p23](../../../assets/images/ce-express/user-guide-v73/p023-img2.png)

3.1.2.2.1 Feature set template
Allows for saving a group of features as a “feature set template”, with one of the features acting as the
origin for the feature set coordinates. The entire feature set can then be placed with a single operation via

![Image p24](../../../assets/images/ce-express/user-guide-v73/p024-img1.png)

![Image p24](../../../assets/images/ce-express/user-guide-v73/p024-img2.png)
the add features tool. Coordinates relative to the origin feature are maintained by the other features in the
set.

General
Feature set template name
Name of the feature set template
Features
Coordinate origin feature
Feature which will be used as the coordinate origin point for the feature set. When the feature set is placed,

![Image p25](../../../assets/images/ce-express/user-guide-v73/p025-img1.png)
this feature will be at the mouse click point.
Feature parameters
Parameters of the features saved in the feature set template. The placed feature parameters will be
automatically filled with the saved values.

3.1.2.2.2 Add Site
Required parameters
| Parameter | Description |
|---|---|
| Site name | Site identification. |
| X | Coordinate in the projected coordinate system. |
| Y | Coordinate in the projected coordinate system. |
Azimuth
Cell direction from the North in degrees.

![Image p29](../../../assets/images/ce-express/user-guide-v73/p029-img1.png)

Optional parameters
| Parameter | Description |
|---|---|
| Height, m | Height above the terrain. |
| Downtilt | Mechanical tilt value. |
| El. Downtilt, deg | Electrical tilt value |
| Frequency | Frequency value in MHz. |
| Power | Power value in dBm. |
| Misc. loss, dB | Miscellaneous loss value in dB. |
| Bandwidth, MHz | Value in MHz. Required for 4G and 5G technologies. For other technologies define the value as 0.015. |
| Noise figure, dB | Value in dB. Required for 4G and 5G technologies. |
Downlink duplex factor
Value range from 0 to 1. Required for Duplex mode TDD, which is applicable for 4G and 5G technologies,
and used for Downlink Throughput calculations. For example, if defined value is 0.7, then 70% of available
bandwidth will be dedicated to Downlink, and 30% - for Uplink.
| Parameter | Description |
|---|---|
| Subcarrier spacing, kHz | Value in kHz. Required for 4G and 5G technologies. For other technologies define value 15. |
| Tx Mimo | Transmitter antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64. |
| Rx Mimo | Receiver antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64. |
Active antenna effect
The parameter is dedicated to smart antenna modeling. The default value is 0, but if massive MIMO is
used, a smart antenna effect can be included to lower the interference and boost throughput.
Recommended values:
- For MIMO 32x32 – value 6.
- For MIMO 64x64 – value 9.
Cell load, %
The parameter is described in percentages and varies from 0 to 100. It describes how the cell is loaded.

The Cell load affects RSSI, RSRQ, and DL Throughput calculations. For example, if the Cell load is higher,
the DL Throughput is lower.
Color index
Describes the cell visualization. Available values:
- None – blue color.
- 1 – red color.
- 2 – light green color.
- 3 – dark green color.
- 4 – light blue color.
- 5 – dark blue color.
- 6 – purple color.
Technology
Describes the technology of the [network object](#kw:object-types:ce-express-network-objects). Possible values are 2G, 3G, 4G, and 5G.
Prediction model
Prediction model for Path Loss simulation.
Frequency group
Used to divide calculations into parts. If the selection range includes two or more different frequency group
values, the cells won’t be predicted together.
Antenna
Define [antenna patterns](#kw:importing-antenna-patterns:ce-express-antenna) for the Cell object.
Carriers
Describes the carrier values used for 2G calculations: C/I interference and C/A interference. The values
are written in brackets, […]. If more than one value is defined, the values are separated by a comma. If
there is no carrier information, the brackets are left empty [].
| Parameter | Description |
|---|---|
| Site ID | Describes to which Site the Cell belongs. |
| Duplex mode | Available values FDD or TDD. Required for 4G and 5G technologies. For other technologies define value FDD. |
| Status | Free-form text. |
| Type | Free-form text. 3.1.2.2.6 Add Repeater |

Required parameters
| Parameter | Description |
|---|---|
| Repeater name | Repeater identification. |
| X | Coordinate in the projected coordinate system. |
| Y | Coordinate in the projected coordinate system. |
| Azimuth | Direction from the North in degrees. |

![Image p32](../../../assets/images/ce-express/user-guide-v73/p032-img1.png)

Optional parameters
| Parameter | Description |
|---|---|
| Height | Object’s height above the terrain. |
| Downtilt | Mechanical tilt in telecommunications repeaters is the physical angling of the antenna to optimize signal coverage. |
| Electrical Tilt | Electrical tilt in a repeater refers to the electronic adjustment of an antenna's vertical radiation pattern to optimize network coverage and reduce interference. |
| Frequency | Frequency value in MHz. |
Thresholds 1, 2, 3
The minimum field strength in dB at repeater location at which power of the corresponding index (1-3) will
be applied. Values should be in ascending order. If a higher threshold is satisfied, the power corresponding
to it will be used.
Power 1, 2, 3
A power that is assigned to cells based on the repeater thresholds and cell signal strength. When the cell’s
signal strength is categorized the power of the repeater will be assigned as well.
Misc loss
Miscellaneous loss value in dB.
Bandwidth
Value in MHz. Required for 4G and 5G technologies. For other technologies define the value as 0.015.
Subcarrier Spacing
Value in kHz. Required for 4G and 5G technologies. For other technologies define value 15.
Tx Mimo
Transmitter antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64.
Rx Mimo
Receiver antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64.
Technology
Describes the technology of the [network object](#kw:object-types:ce-express-network-objects).
Prediction Model
Lets the user select which prediction model and configuration should be used for calculations.
Frequency group
Used to divide calculations into parts. If the selection range includes two or more different frequency group
values, the cells won’t be predicted together.

Antenna
Antenna name for Repeater object.
3.1.2.2.7 Add Radar
Required parameters
| Parameter | Description |
|---|---|
| Radar name | Radar identification. |
| X | Coordinate in the projected coordinate system. |
| Y | Coordinate in the projected coordinate system. |
Optional parameters
Height
Object’s height above the terrain.

![Image p34](../../../assets/images/ce-express/user-guide-v73/p034-img1.png)

| Parameter | Description |
|---|---|
| Downtilt | Mechanical tilt value. |
| Frequency | Frequency value in MHz. |
| Power | Power value in dBm. |
| Misc Loss | Miscellaneous loss value in dB. |
| View Angle | Visible field (vertical angle) of the radar in degrees. |
| Prediction Model | Prediction model for Path Loss simulation. 3.1.2.2.8 Add CPE |

![Image p35](../../../assets/images/ce-express/user-guide-v73/p035-img1.png)

Required parameters
| Parameter | Description |
|---|---|
| CPE name | CPE identification. |
| X | Coordinate in the projected coordinate system. |
| Y | Coordinate in the projected coordinate system. |
Optional parameters
Height
Object’s height above the terrain.
Azimuth
Direction from the North in degrees.
Antenna
Antenna name for CPE location.
Power
A power value in dBm.
Misc loss
Miscellaneous loss value in dB.
Cell ID
Describes to which Cell the CPE point belongs.
Throughput
The speed at which data is transferred. Measured in Mb/s.
Status
Current status of the [network object](#kw:object-types:ce-express-network-objects).
Notes
Additional information for network predictions can be noted here.
3.1.2.2.9 Add Measurements

Required parameters
| Parameter | Description |
|---|---|
| Field strength, dB | Field strength. |
| X | Coordinate in the projected coordinate system. |
| Y | Coordinate in the projected coordinate system. |
| Cell ID | A field which binds the measurement to a cell network object. 3.1.2.2.10 Add Omen |
3.1.2.2.10 Add Omen

![Image p37](../../../assets/images/ce-express/user-guide-v73/p037-img1.png)

![Image p37](../../../assets/images/ce-express/user-guide-v73/p037-img2.png)

Required parameters
| Parameter | Description |
|---|---|
| Omen name | Omen identification. |
| X | Coordinate in the projected coordinate system. |
| Y | Coordinate in the projected coordinate system. |
Optional parameters
Height, m
Height above the terrain.
Notes
Free-form text.
3.1.2.2.11 Add Sirens

![Image p38](../../../assets/images/ce-express/user-guide-v73/p038-img1.png)

Required parameters
| Parameter | Description |
|---|---|
| Siren name | Siren identification. |
| X | Coordinate in the projected coordinate system. |
| Y | Coordinate in the projected coordinate system. |
| Azimuth | Cell direction from the North in degrees. |
Optional parameters
| Parameter | Description |
|---|---|
| Height, m | Height above the terrain. |
| Downtilt | Mechanical tilt value. |
| Frequency | Frequency value in MHz. |
| Power | Power value in dBm. |
| Misc. loss, dB | Miscellaneous loss value in dB. |
| Prediction model | Only ISO9613 can be applied to calculate sound loss for the siren. |
| Antenna | Antenna name for Siren object. |
| Status | Free-form text. |
| Type | Free-form text. 3.1.2.2.12 Add Lights |

Required parameters
| Parameter | Description |
|---|---|
| Light name | Light identification. |
| X | Coordinate in the projected coordinate system. |
| Y | Coordinate in the projected coordinate system. |
| Azimuth | Cell direction from the North in degrees. |
Optional parameters
Height, m
Height above the terrain.
Downtilt
Mechanical tilt value.

![Image p40](../../../assets/images/ce-express/user-guide-v73/p040-img1.png)

Antenna
Antenna name for Light object.
3.1.2.2.13 Add Mesh nodes
Required parameters
| Parameter | Description |
|---|---|
| Mesh node name | Mesh node identification. |
| X | Coordinate in the projected coordinate system. |
| Y | Coordinate in the projected coordinate system. |

![Image p41](../../../assets/images/ce-express/user-guide-v73/p041-img1.png)

Optional parameters
Height, m
Height above the terrain.
Frequency, MHz
Frequency of the mesh node.
Power, dBm
Power value of the mesh node.
Misc Loss, dB
Miscellaneous loss value of the mesh node.
Prediction model
The prediction model that will be used for the mesh node in Mesh Connectivity and Quick Mesh Connectivity
calculations.
Antenna
Define [antenna patterns](#kw:importing-antenna-patterns:ce-express-antenna) for the mesh node object.
Sensitivity
Sensitivity value of the mesh node.
Max connections
The maximum number of connections the mesh node can have (used for mesh connectivity calculations).
Layer
The layer of the mesh node (number value). Used for priority calculations in Automatic Frequency Planning.

![Image p42](../../../assets/images/ce-express/user-guide-v73/p042-img1.png)
Group name
The group name of the mesh node (text description). Several mesh nodes may belong to the same group.
Status
Free-form text.
Type
Free-form text.
3.1.2.3 Selecting

Selection settings
Show only selected features
Only the selected features will be displayed in the feature list. When the switch off, all features are visible

![Image p43](../../../assets/images/ce-express/user-guide-v73/p043-img1.png)

![Image p43](../../../assets/images/ce-express/user-guide-v73/p043-img2.png)

![Image p43](../../../assets/images/ce-express/user-guide-v73/p043-img3.png)
regardless of selection. When it is on non-selected features are hidden, so you see only what you have
selected.
Mode
There are several different modes for [selecting objects](#kw:selecting-multiple-objects:ce-express-network-objects):
- Rectangle.
To start the selection process, click once on the map, then move the mouse cursor to define an
area, click a second time to finish the selection process.
- Single click. Click once on an object to select it.

- Radius.
Set the desired distance, then click on the map and the surrounding objects within the set distance will

![Image p44](../../../assets/images/ce-express/user-guide-v73/p044-img1.png)

![Image p44](../../../assets/images/ce-express/user-guide-v73/p044-img2.png)

![Image p44](../../../assets/images/ce-express/user-guide-v73/p044-img3.png)
be selected.
- Polygon.

Click once on the map to create the vertices of the polygon. Double-click to close the polygon and select

![Image p45](../../../assets/images/ce-express/user-guide-v73/p045-img1.png)

![Image p45](../../../assets/images/ce-express/user-guide-v73/p045-img2.png)
the feature.
- Polygon layer.
To use the polygon layer selection, choose a predefined polygon layer from the dropdown list. Then,
click on the map. All features located within the selected polygon boundary will be highlighted and
displayed in the feature list.

Selected objects will be highlighted on the map and listed in the tool.

![Image p46](../../../assets/images/ce-express/user-guide-v73/p046-img1.png)

![Image p46](../../../assets/images/ce-express/user-guide-v73/p046-img2.png)

Clear selection
Clears a objects selection on the map.
Search
Initiates the search procedure in the selected objects list.
Show in table
Opens the selected objects attribute table
3.1.2.4 Move/Duplicate/Delete/Publish selected objects
Select objects on the map to start the Publish, Move, Duplicate or Delete functionality.
Publish
Select the features you want to publish to portal as a feature layer, then click the publish button.

![Image p47](../../../assets/images/ce-express/user-guide-v73/p047-img1.png)

![Image p47](../../../assets/images/ce-express/user-guide-v73/p047-img2.png)

![Image p47](../../../assets/images/ce-express/user-guide-v73/p047-img3.png)
An option menu then appears to let you select who the newly created feature layer will be shared to:

Press OK to start the publishing process.
Move
Select the objects which shall be moved and choose the Move tool. The Move selected features dialog will
appear.
Hold the left mouse button and drag the object to the preferred location.
Press Accept to save changes.
Duplicate
Select the objects which shall be duplicated and choose the Duplicate tool. The Duplicate features dialog
will appear. Hold the left mouse button and drag the object to the preferred location. Selected objects can

![Image p48](../../../assets/images/ce-express/user-guide-v73/p048-img1.png)

![Image p48](../../../assets/images/ce-express/user-guide-v73/p048-img2.png)

![Image p48](../../../assets/images/ce-express/user-guide-v73/p048-img3.png)
be duplicated to another workspace.

Press Accept to save changes.
Delete
Select the objects on the map, then press the Delete button to remove them from the Map view and
database tables.
Press Accept to save changes.
3.1.2.5 Edit objects
Object attributes can be edited using the Cellular Expert graphical interface. Move the mouse cursor to the

![Image p49](../../../assets/images/ce-express/user-guide-v73/p049-img1.png)

![Image p49](../../../assets/images/ce-express/user-guide-v73/p049-img2.png)
required object in the Features tool and click on it to edit object attributes.

A new dialog opens on the right side with the most important attributes.

![Image p50](../../../assets/images/ce-express/user-guide-v73/p050-img1.png)

Accept
Saves all changes.
Cancel
Discards all changes and closes the dialog.
Upon hovering the mouse over a feature item, options for it appear.

![Image p51](../../../assets/images/ce-express/user-guide-v73/p051-img1.png)

![Image p51](../../../assets/images/ce-express/user-guide-v73/p051-img2.png)

| Parameter | Description |
|---|---|
| View from perspective | Viewpoint from the position of cell. |
| Highlight feature | Highlights feature on the map. |
| Duplicate feature | Creates a copy of the feature. |
| Delete feature | Deletes feature. |
| Remove from selection | Removes feature from the selected features list. |
Add to selection
Adds feature to selected features list.
3.1.2.6 Quick add
If you have feature templates favorited, the quick add section will appear under the feature type in the
features list. You may then use the listed favorite feature templates to quickly add features with the template

![Image p52](../../../assets/images/ce-express/user-guide-v73/p052-img1.png)

![Image p52](../../../assets/images/ce-express/user-guide-v73/p052-img2.png)

![Image p52](../../../assets/images/ce-express/user-guide-v73/p052-img3.png)

![Image p52](../../../assets/images/ce-express/user-guide-v73/p052-img4.png)

![Image p52](../../../assets/images/ce-express/user-guide-v73/p052-img5.png)

![Image p52](../../../assets/images/ce-express/user-guide-v73/p052-img6.png)

![Image p52](../../../assets/images/ce-express/user-guide-v73/p052-img7.png)
applied. This can be done in 2 ways:
- Click the feature template name to automatically open the add features tool and have the template
applied
- Drag and drop the feature template on the map to quickly add a new feature to the desired location
with only having the enter the feature name in a popup.
