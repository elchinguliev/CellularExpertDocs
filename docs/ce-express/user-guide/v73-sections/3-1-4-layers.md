# 3.1.4 Layers

Click this button to open Layers tool.
Manages the visualization of features and calculation results in the Map view. Displays and manages all
layers in the workspace, grouped into categories such as Features, Geodata, Prediction results, and
Other. Each layer can be shown, hidden, or reordered.
You can reorder the entire group or toggle its visibility to show or hide all layers within it at once.

![Image p59](../../../assets/images/ce-express/user-guide-v73/p059-img1.png)

![Image p59](../../../assets/images/ce-express/user-guide-v73/p059-img2.png)

Layers can also be organized by dragging them into existing groups or dropping them into New layer group

![Image p60](../../../assets/images/ce-express/user-guide-v73/p060-img1.png)

![Image p60](../../../assets/images/ce-express/user-guide-v73/p060-img2.png)
to create a custom group.
3.1.4.1 Add layer
Layers added from this panel are visible only to you. Other users who open the same workspace will not
see these layers unless they also add them manually.

From URL / Portal ItemID
Allows you to add a layer directly by entering its URL or Portal Item ID, then selecting Add.
Search criteria
My organization
Limits search results to layers shared within your organization.

![Image p61](../../../assets/images/ce-express/user-guide-v73/p061-img1.png)

| Parameter | Description |
|---|---|
| Owned by me | Shows only layers you own. |
| Sort by | Determines the order of search results (e.g., by view count or date). 3.1.4.2 Features |
| Rearrange layers | Allows you to reorder layers by dragging. |
| Turn on/off the layer | Turn on or off a layer in the Map view • The layer is visible - The layer is not visible - • |

![Image p62](../../../assets/images/ce-express/user-guide-v73/p062-img1.png)

![Image p62](../../../assets/images/ce-express/user-guide-v73/p062-img2.png)

![Image p62](../../../assets/images/ce-express/user-guide-v73/p062-img3.png)

![Image p62](../../../assets/images/ce-express/user-guide-v73/p062-img4.png)

Layer symbol
Preview layer symbol. Click on it to edit the symbol.
Expand layer
Previews and manages the layer opacity and map scale .
3.1.4.2.1 Edit symbolization
Click on the layer symbol to edit it. A new dialog opens on the right side.

![Image p63](../../../assets/images/ce-express/user-guide-v73/p063-img1.png)

![Image p63](../../../assets/images/ce-express/user-guide-v73/p063-img2.png)

![Image p63](../../../assets/images/ce-express/user-guide-v73/p063-img3.png)

In layer symbolization it is possible to change:
- Shape.
o if a path is selected in shape, svg path can be changed.
- Size.
- Color.
- Turn on and off outline.
- Outline color.
- Turn on and off offset.
- X/Y offset.

![Image p64](../../../assets/images/ce-express/user-guide-v73/p064-img1.png)

There is an option to use 3d symbol. The following parameters can be changed in the 3d symbol:
- Shape
- Color
- Width
- Height
- Tilt
Visual variables can be added for each layer. Add visual variables to a layer using the Add visual variable

![Image p65](../../../assets/images/ce-express/user-guide-v73/p065-img1.png)

![Image p65](../../../assets/images/ce-express/user-guide-v73/p065-img2.png)
dropdown.

Choose a visual variable. The choices are:
- Color.
- Size.
- Rotation.
- Opacity.
Accept
Saves all changes.
Cancel
Discards all changes and closes the dialog.

![Image p66](../../../assets/images/ce-express/user-guide-v73/p066-img1.png)

3.1.4.3 Prediction results
The prediction rasters calculated in Cellular Expert Express and loaded in the map view will appear in the

![Image p67](../../../assets/images/ce-express/user-guide-v73/p067-img1.png)

![Image p67](../../../assets/images/ce-express/user-guide-v73/p067-img2.png)

![Image p67](../../../assets/images/ce-express/user-guide-v73/p067-img3.png)

![Image p67](../../../assets/images/ce-express/user-guide-v73/p067-img4.png)
Layers tool.
| Parameter | Description |
|---|---|
| Rearrange layers | Allows you to reorder layers by dragging. |
| Turn on/off the layer | Turn on or off a layer in the Map view The layer is visible - • The layer is not visible - • |
| Expand layer | Expand the layer so you can see and edit the symbology. |

For these types of layers, the visualization can be edited in the following ways:
- Add threshold using Add color band button
- Adjust threshold value
- Adjust color band
- Adjust color opacity
- Delete threshold using Delete band button
Upon hovering the mouse over a prediction result item, options for it appear.

![Image p68](../../../assets/images/ce-express/user-guide-v73/p068-img1.png)

![Image p68](../../../assets/images/ce-express/user-guide-v73/p068-img2.png)

![Image p68](../../../assets/images/ce-express/user-guide-v73/p068-img3.png)

![Image p68](../../../assets/images/ce-express/user-guide-v73/p068-img4.png)

![Image p68](../../../assets/images/ce-express/user-guide-v73/p068-img5.png)

Rename layer
Publish to portal
Zoom to layer
[Compare](#kw:98-compare-predictions:ce-pro-rcp)
Remove layer
3.1.4.3.1 Presets
It is possible to create symbology presets. This means that when a prediction raster is loaded, a symbology
preset can be used:

To create a preset, first define the bands and colors, then press New color band preset button.
Define a preset name.
A new preset will be created.
The defined preset will be applied the next time when the raster will be loaded.
Apply
Applies a preset symbology for the current prediction raster layer.
3.1.4.3.2 Swipe
The Swipe widget enables you to easily [compare](#kw:98-compare-predictions:ce-pro-rcp) the content of different layers in a map. Mouse over the
layers you want to compare and press the compare button.
When the first and second layers are selected for comparison, a swipe widget will appear on

![Image p70](../../../assets/images/ce-express/user-guide-v73/p070-img1.png)

![Image p70](../../../assets/images/ce-express/user-guide-v73/p070-img2.png)

![Image p70](../../../assets/images/ce-express/user-guide-v73/p070-img3.png)

![Image p70](../../../assets/images/ce-express/user-guide-v73/p070-img4.png)

![Image p70](../../../assets/images/ce-express/user-guide-v73/p070-img5.png)

![Image p70](../../../assets/images/ce-express/user-guide-v73/p070-img6.png)

![Image p70](../../../assets/images/ce-express/user-guide-v73/p070-img7.png)
the map. Slide the swipe tool to compare different layers.

3.1.4.3.3 Publish to portal
Raster prediction results may be individually published to portal by using the publish to portal button.

![Image p71](../../../assets/images/ce-express/user-guide-v73/p071-img1.png)

![Image p71](../../../assets/images/ce-express/user-guide-v73/p071-img2.png)
Upon clicking this button, publishing settings will appear:
Set up the publishing options and click OK to start the publishing process.
3.1.4.4 Geodata
This section appears when enabled in the settings.

Section contains geodata raster layers from the geodata set assigned to the current workspace.
- Elevation:

![Image p72](../../../assets/images/ce-express/user-guide-v73/p072-img1.png)

![Image p72](../../../assets/images/ce-express/user-guide-v73/p072-img2.png)

![Image p72](../../../assets/images/ce-express/user-guide-v73/p072-img3.png)

- Clutter height:
- [Clutter classes](#kw:clutter-classification-values:ce-express-geodata):
