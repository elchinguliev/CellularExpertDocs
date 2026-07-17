# Layers

> **Version:** CE Express v7.3

The Layers tool manages the visualization of features and calculation results in the Map view. It displays all layers in the workspace, grouped into categories: Features, Geodata, Prediction results, and Other.

---

3.1.4 Layers
Click this button to open Layers tool.
Manages the visualization of features and calculation results in the Map view. Displays and manages all
layers in the workspace, grouped into categories such as Features, Geodata, Prediction results, and
Other. Each layer can be shown, hidden, or reordered.
You can reorder the entire group or toggle its visibility to show or hide all layers within it at once.

Layers can also be organized by dragging them into existing groups or dropping them into New layer group
to create a custom group.
3.1.4.1 Add layer
Layers added from this panel are visible only to you. Other users who open the same workspace will not
see these layers unless they also add them manually.

From URL / Portal ItemID
Allows you to add a layer directly by entering its URL or Portal Item ID, then selecting Add.
Search criteria
My organization
Limits search results to layers shared within your organization.

Owned by me
Shows only layers you own.
Sort by
Determines the order of search results (e.g., by view count or date).
3.1.4.2 Features
Rearrange layers
Allows you to reorder layers by dragging.
Turn on/off the layer
Turn on or off a layer in the Map view
• The layer is visible -
• The layer is not visible -

Layer symbol
Preview layer symbol. Click on it to edit the symbol.
Expand layer
Previews and manages the layer opacity and map scale .
3.1.4.2.1 Edit symbolization
Click on the layer symbol to edit it. A new dialog opens on the right side.

In layer symbolization it is possible to change:
• Shape.
o if a path is selected in shape, svg path can be changed.
• Size.
• Color.
• Turn on and off outline.
• Outline color.
• Turn on and off offset.
• X/Y offset.

There is an option to use 3d symbol. The following parameters can be changed in the 3d symbol:
• Shape
• Color
• Width
• Height
• Tilt
Visual variables can be added for each layer. Add visual variables to a layer using the Add visual variable
dropdown.

Choose a visual variable. The choices are:
• Color.
• Size.
• Rotation.
• Opacity.
Accept
Saves all changes.
Cancel
Discards all changes and closes the dialog.

3.1.4.3 Prediction results
The prediction rasters calculated in Cellular Expert Express and loaded in the map view will appear in the
Layers tool.
Rearrange layers
Allows you to reorder layers by dragging.
Turn on/off the layer
Turn on or off a layer in the Map view
• The layer is visible -
• The layer is not visible -
Expand layer
Expand the layer so you can see and edit the symbology.

For these types of layers, the visualization can be edited in the following ways:
• Add threshold using Add color band button
• Adjust threshold value
• Adjust color band
• Adjust color opacity
• Delete threshold using Delete band button
Upon hovering the mouse over a prediction result item, options for it appear.

Rename layer
Publish to portal
Zoom to layer
Compare
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
The Swipe widget enables you to easily compare the content of different layers in a map. Mouse over the
layers you want to compare and press the compare button.
When the first and second layers are selected for comparison, a swipe widget will appear on
the map. Slide the swipe tool to compare different layers.

3.1.4.3.3 Publish to portal
Raster prediction results may be individually published to portal by using the publish to portal button.
Upon clicking this button, publishing settings will appear:
Set up the publishing options and click OK to start the publishing process.
3.1.4.4 Geodata
This section appears when enabled in the settings.

Section contains geodata raster layers from the geodata set assigned to the current workspace.
• Elevation:

• Clutter height:
• Clutter classes:
3.1.5 Prediction history
Click this button to open Prediction history tool.
