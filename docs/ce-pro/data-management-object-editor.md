# Data Management — Object Editor

> **Note:** RLP has additional link-specific object editor actions (Move/Duplicate Link Objects, Move/Duplicate Site Objects) — see the RLP guide content if this differs on your build. "Calculate Cells Area" below is an RCP-only feature.

### 7.3 Object Editor
The Object Editor enables the user to make changes to a network object after it is created and placed on
the map.
Choose the button to open the Object Editor dialogue.
Select objects by navigating to the ArcGIS Pro Edit → Selection section and choosing the Select tool. The
selected objects will appear in the Object Editor in a tree hierarchy.

To edit one of the selected objects, left-click on that object and the corresponding editing menu will open

![Image p79](../assets/images/ce-pro/rcp-guide/p079-img1.png)

![Image p79](../assets/images/ce-pro/rcp-guide/p079-img2.png)
below the list.
Delete Object
Select and right-click any network object from the selection, then choose the Delete option from the popup.

Duplicate Object
Select and right-click any object from the selection, then choose the Duplicate option from the popup. The
duplicated object will retain all information from the original object including coordinates/meridians. If you

![Image p80](../assets/images/ce-pro/rcp-guide/p080-img1.png)

![Image p80](../assets/images/ce-pro/rcp-guide/p080-img2.png)
want to duplicate objects and change their coordinates/meridians at the same time, use the separate
Duplicate Objects button from above the selection tree.

#### 7.3.1 Move Objects
Choose the button to open the Object Editor dialogue. Select the desirable objects with the Select
tool and press the Move Objects button in the Object Editor.

There are multiple ways to move objects:
• If multiple objects are selected, the move objects display will show the geospatial properties of the

![Image p81](../assets/images/ce-pro/rcp-guide/p081-img1.png)
center point between the objects denoted as the “Cursor point”.

The "Cursor Point" functions as a reference marker depicted by a red dot on the map. This marker is
centrally located among the objects on the map and shows where the cursor was placed. You can adjust
the position of the Cursor Point either by entering new coordinates directly or by clicking “Select Point” and

![Image p82](../assets/images/ce-pro/rcp-guide/p082-img1.png)

![Image p82](../assets/images/ce-pro/rcp-guide/p082-img2.png)
choosing a different location on the map. When you move the Cursor Point, all the objects on the map will
shift their position to maintain their relative distances from this central point.
• If a single point object is selected or several objects at the same location, the move objects display

will show the geospatial properties of these objects denoted as “Cursor Point”.
If a single point object is selected on the map, the "Cursor Point" serves as its positional anchor. Positioned

![Image p83](../assets/images/ce-pro/rcp-guide/p083-img1.png)
as a red dot, the Cursor Point represents the current coordinates of the selected object and shows where
the cursor was last placed. You can alter the location of the selected object by manually updating the Cursor
Point's coordinates or by clicking “Select Point” and choosing a new location on the map. Any movement
of the Cursor Point will directly translate the selected object to the corresponding new location while keeping
its spatial relationship with the Cursor Point consistent.

Save Changes
Saves the changes to the objects.
Dismiss
Cancels the changes to the objects and closes the dialogue.

#### 7.3.2 Duplicate Objects
Choose the button to open the Object Editor dialogue. Select the object with the Select tool and

![Image p84](../assets/images/ce-pro/rcp-guide/p084-img1.png)

![Image p84](../assets/images/ce-pro/rcp-guide/p084-img2.png)
press the Duplicate Objects button in the Object Editor dialogue.

There are multiple ways to duplicate objects:
• If multiple objects are selected, the duplicate objects display will show the geospatial properties of
the center point between the objects denoted as the “Cursor point”.
The "Cursor Point" functions as a reference marker depicted by a red dot on the map. This marker is
centrally located among the objects on the map and shows where the cursor was placed. You can adjust
the position of the Cursor Point either by entering new coordinates directly or by clicking “Select Point” and

![Image p85](../assets/images/ce-pro/rcp-guide/p085-img1.png)
choosing a different location on the map. When you move the Cursor Point, all the objects on the map will
shift their position to maintain their relative distances from this central point.

• If a single point object or several objects on the same location are selected, the duplicate objects

![Image p86](../assets/images/ce-pro/rcp-guide/p086-img1.png)

![Image p86](../assets/images/ce-pro/rcp-guide/p086-img2.png)
display will show the geospatial properties of that object denoted as “Cursor Point”.

If a single point object is selected on the map, the "Cursor Point" serves as its positional anchor. Positioned

![Image p87](../assets/images/ce-pro/rcp-guide/p087-img1.png)

![Image p87](../assets/images/ce-pro/rcp-guide/p087-img2.png)
as a red dot, the Cursor Point represents the current coordinates of the selected object and also shows
where the cursor was last placed. You can alter the location of the selected object by manually updating
the Cursor Point's coordinates or by clicking “Select Point” and choosing a new location on the map. Any
movement of the Cursor Point will directly translate the selected object to the corresponding new location
while keeping its spatial relationship with the Cursor Point consistent.
Save Changes
Duplicates the objects.
Dismiss
Cancels the changes to the objects and closes the dialogue.

### 7.4 Calculate Cells Area
The Calculate Cells Area tool is designed to compute the service areas of selected cell sites within a given
map and display them as polygons in a new layer. By selecting one or more cells, users can initiate a
calculation that considers various parameters like cell azimuth, horizontal beamwidth, and antenna patterns
to generate precise coverage polygons.
Choose the button to open the Calculate Cells Area tool.

Select the cells which the calculations will be performed for, and press Run Calculation. The cell areas
will be drawn on the map, in a separate layer CE Cell Area Results. In the results group layer, the servitude

![Image p88](../assets/images/ce-pro/rcp-guide/p088-img1.png)

![Image p88](../assets/images/ce-pro/rcp-guide/p088-img2.png)

![Image p88](../assets/images/ce-pro/rcp-guide/p088-img3.png)
polygons can be toggled for each cell.
The polygons represent the cell area where the antenna’s horizontal pattern’s attenuation at each angle is
lower than the threshold of 3.

Maximum radius depends on defined Prediction Model, Radius value for the Cell object.
Using bigger radius:
