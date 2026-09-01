# MAP functionality

Users can work with maps only after prior configuration by the administrator. Select a site and open the map:

![Map opened for a selected site](../../assets/images/inventory3d/user-guide/p030-fig2-mapview-open.png)

**Map viewing options**

On the right side of the screen, you find the commands

Full screen ![icon](../../assets/images/inventory3d/user-guide/p031-icon-fullscreen.png) - Google Street View ![icon](../../assets/images/inventory3d/user-guide/p031-icon-streetview.png) - Zoom in / out ![icon](../../assets/images/inventory3d/user-guide/p031-icon-zoominout.png)

Map view - select the preferred map background, for example ESRI streets:

![Map with the map background selector set to ESRI Streets](../../assets/images/inventory3d/user-guide/p031-fig1-mapview-esri.png)

**Home**

![icon](../../assets/images/inventory3d/user-guide/map-home.png) Moves the map view to your current location.

**Measure Distances**

Select the Measure Tool
![icon](../../assets/images/inventory3d/user-guide/map-measure-tool.png), left-click on the starting point, then move the mouse over the map - distance and azimuth values will be displayed between the starting point and the mouse cursor.

**Link to database**



Map and database are functionally connected. Select the info tool ![Info tool icon](../../assets/images/inventory3d/user-guide/map-information-tool.png). Then click on a site in the map (here: Abava), and a popup window opens:

![Popup window with site attribute information after clicking a site on the map](../../assets/images/inventory3d/user-guide/p032-fig1-linktodb-popup.png)

The popup window comprises links to the site (![Site link icon in the popup window](../../assets/images/inventory3d/user-guide/map-site-link.png)) and to the attachments file browser (![Attachments file browser icon in the popup window](../../assets/images/inventory3d/user-guide/map-attachments.png))

Browse the parameters of the selected site by using the buttons
![Browse buttons used to page through the site parameters](../../assets/images/inventory3d/user-guide/map-browse-buttons.png).

**Local Weather**



Display local weather conditions by clicking on ![Weather tool icon](../../assets/images/inventory3d/user-guide/map-weather-tool.png) and then on a custom position on the map. A popup window opens with the local weather information. Users may choose from daily, weekly, and monthly data:

![Local weather popup with current weather information](../../assets/images/inventory3d/user-guide/p033-fig1-localweather-popup.png)

**Address search**

Use the field "Search in Google Maps" to search an address and zoom to the defined address.

**Print map**

Custom map views can be exported and printed. In the Map toolbar, click the print button ![Print button in the map toolbar](../../assets/images/inventory3d/user-guide/map-print.png) .

A popup window opens with the possibility to enter a document header. Then send the selected map view to the printer with ![icon](../../assets/images/inventory3d/user-guide/p033-icon-printbutton2.png) or ![icon](../../assets/images/inventory3d/user-guide/p033-icon-pngbutton.png):

![Print map popup with a document header field](../../assets/images/inventory3d/user-guide/p034-fig1-printmap-dialog.png)

**Vectors, Rasters and Weather layers**

![Layers panel listing vector, raster and weather layers](../../assets/images/inventory3d/user-guide/p034-fig2-vectors-rasters-weather.png)

The map functionality allows to show or hide vectors (points, lines), rasters or weather layers.

Use the ![icon](../../assets/images/inventory3d/user-guide/map-layer-show.png) and ![icon](../../assets/images/inventory3d/user-guide/map-layer-hide.png) to show or hide objects.

Further, it is possible to select the child objects shown on the map:

![Layers panel with a layer expanded to show its child objects](../../assets/images/inventory3d/user-guide/p035-fig1-layers-childobjects.png)

Additional map functions are shown after clicking the menu icon ![Menu icon used to show additional map functions](../../assets/images/inventory3d/user-guide/map-layer-menu.png) .

![Layer menu with additional map functions listed](../../assets/images/inventory3d/user-guide/p035-fig2-layers-additionalfns.png)

"Reload" allows to reload the layer. Edit an object and click "Reload" to show the map with the edited features.

"Add Object" allows to add an object to the map.

1. Select the layer on which You would like to add an object, for example "site". Then click "Add Object".
2. Click to the position on the map where you would like to add a new object. If the layer consists of lines, you need to click on the map two times for each end of the line.
3. An object will be created without a label (if label was not described in inv3d_map_settings).
4. Use the info tool ![Info tool icon](../../assets/images/inventory3d/user-guide/map-information-tool.png) to open the Inventory3D page for the new object, edit the attributes and save the information to the database.
5. Click "Reload" and the map will be reloaded with the newly added attributes, for example a label.

"Move Object" allows to move an object of point type on the map

1. Select the layer on which You would like to move an object, for example "site". Then click "Select Object".
2. Select the object on the map (it should be marked with a square).
3. Move the pointer to the desired position on the map. Click and the selected object will be moved to the new position. The function will not work if two or more objects are selected.

"Set Filter" allows to filter the objects shown on the map.

For example, only sites with the address equal to Riga are shown:

![Set Filter panel with ADDRESS = Riga](../../assets/images/inventory3d/user-guide/p036-fig1-setfilter-example.png)

If the condition *like* is selected, as in the example below, only objects with the address containing Riga will be displayed.

![Set Filter panel with ADDRESS like Riga](../../assets/images/inventory3d/user-guide/p036-fig2-setfilter-like.png)

"Clear Filter" allows to clear a preset filter.

"Select Object" allows to select one object from the map.

To select an object, first click "Select Object" and then on the object on the map.

"Select Circular Area" and "Select Rectangular Area" allow to select multiple objects on the map.

1. Click "Select Circular Area" or "Select Rectangular Area".
2. Click the mouse button on the map and release.
3. Move the mouse to select several objects and click the mouse button again to release.
4. Selected objects are marked with a yellow square:

   ![Selected object marked with a yellow square](../../assets/images/inventory3d/user-guide/p037-fig1-yellowsquare.png)

"Open Selection" Allows to open the CE Inventory3D attribute information of the selected objects. Click "Open Selection" and a new browser tab opens with the grouped data for the selected objects.

"Draw Circles & Vectors" Allows to draw circles with a defined radius and lines with a defined azimuth for selected objects. This feature must be configured by the administrator. It draws vectors based on data defined in the tables `[table]_circles` and `[table]_vectors`, where table is the name of layer table.

"Clear Selection & Vectors" Allows to clear all selections, drawn circles and vectors.

Just as the Vectors, Raster and Weather layers, for example the current weather, are shown or hidden the buttons ![icon](../../assets/images/inventory3d/user-guide/map-layer-show.png) and ![icon](../../assets/images/inventory3d/user-guide/map-layer-hide.png) .
