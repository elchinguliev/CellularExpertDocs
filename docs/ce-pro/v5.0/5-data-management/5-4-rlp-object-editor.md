# RLP Object Editor

> **Applies to:** RLP. For SAT, Sound, EMF, Indoor, and RCP, see the shared [Object Editor](5-3-object-editor.md).

The Object Editor lets you change a network object after it has been created and placed on the map. RLP's Object Editor is structurally different from the shared Object Editor — it handles Link (line) objects and Site (point) objects separately.

Choose the Object Editor button to open the dialog. Select objects by navigating to the ArcGIS Pro **Edit > Selection** section and choosing the Select tool — the selected objects appear in the Object Editor as a tree hierarchy. To edit one of the selected objects, left-click on it and the corresponding editing menu opens below the list.

![RLP Object Editor tree with a Duplicate/Delete context menu on a Link object](../../../assets/images/ce-pro/v5.0/rlp-object-editor-tree.png)

## Delete Object

Select and right-click any network object from the selection, then choose **Delete** from the popup.

## Duplicate Object

Select and right-click any object from the selection, then choose **Duplicate** from the popup. The duplicated object retains all information from the original, including coordinates/meridians. To duplicate objects and change their coordinates/meridians at the same time, use the separate **Duplicate Objects** button above the selection tree.

## Move Link Objects

Choose the Object Editor button to open the dialog. Select the desired Link objects with the Select tool, then press **Move Objects**.

The Link object has separate **Transmitter** and **Receiver** parameter panels.

![Object Editor — Receiver Point parameters for a Link](../../../assets/images/ce-pro/v5.0/rlp-move-link-receiver-point.png)

The location of the Transmitter and Receiver can be changed:

- By defining exact coordinates in the Transmitter and Receiver sections.
- Using the **Select Tx** and **Select Rx** buttons.

If a new location is defined, the potential link is shown on the map. Pressing **Save Changes** moves both the Link and its Site objects.

| Button | Description |
|---|---|
| Save Changes | Saves the changes to the objects. |
| Dismiss | Cancels the changes to the objects and closes the dialog. |

## Duplicate Link Objects

Choose the Object Editor button to open the dialog. Select the Link object with the Select tool, then press **Duplicate Objects**.

The Link object again has separate Transmitter and Receiver parameter panels. The location of the Transmitter and Receiver can be changed:

- By defining exact coordinates in the Transmitter and Receiver sections.
- Using the **Select Tx** and **Select Rx** buttons.

If a new location is defined, the potential link is shown on the map. Pressing **Save Changes** duplicates both the Link and its Site objects.

| Button | Description |
|---|---|
| Save Changes | Saves the changes to the objects. |
| Dismiss | Cancels the changes to the objects and closes the dialog. |

## Move Site (Point) Objects

Choose the Object Editor button to open the dialog. Select the desired objects with the Select tool, then press **Move Objects**.

There are multiple ways to move objects:

- **If multiple objects are selected**, the Move Objects display shows the geospatial properties of the center point between the objects, denoted as the **Cursor Point**. The Cursor Point is a reference marker shown as a red dot on the map, centrally located among the selected objects. You can adjust its position by entering new coordinates directly, or by clicking **Select Point** and choosing a different location on the map. Moving the Cursor Point shifts all objects to maintain their relative distances from this central point.
- **If a single point object is selected (or several objects at the same location)**, the Move Objects display shows the geospatial properties of that object, also denoted as the **Cursor Point** — the object's positional anchor. You can move the object by manually updating the Cursor Point's coordinates, or by clicking **Select Point** and choosing a new location on the map. Any movement of the Cursor Point directly translates the object to the new location.

| Button | Description |
|---|---|
| Save Changes | Saves the changes to the objects. |
| Dismiss | Cancels the changes to the objects and closes the dialog. |

## Duplicate Site (Point) Objects

Choose the Object Editor button to open the dialog. Select the object with the Select tool, then press **Duplicate Objects**.

There are multiple ways to duplicate objects:

- **If multiple objects are selected**, the Duplicate Objects display shows the geospatial properties of the center point between the objects, denoted as the **Cursor Point** — behaving the same way as in Move Objects.
- **If a single point object (or several objects at the same location) is selected**, the Duplicate Objects display shows the geospatial properties of that object, denoted as the **Cursor Point** — the object's positional anchor.

| Button | Description |
|---|---|
| Save Changes | Duplicates the objects. |
| Dismiss | Cancels the changes to the objects and closes the dialog. |
