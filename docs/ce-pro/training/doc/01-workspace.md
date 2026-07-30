**Cellular Expert**

**1. Creating Workspace**

\
=

# Objective

This tutorial demonstrates how to create a personal geodatabase for use with Cellular Expert in a single-use configuration and introduces basic functions. By the end of the exercise, you will be able to:

- Create ArcGIS Pro project.

- Create a new Cellular Expert database.

- Add and manage topographical data.

## Single-User Environment

For the Single-User configuration of Cellular Expert, all information about radio network objects is stored in a personal geodatabase (GDB format) or locally on the disc (calculation results, raster data in GeoTIFF format, etc.).

# Create CE Workspace

## Create ArcGIS Pro project

This guide outlines the steps for creating and saving an ArcGIS Pro project, where we will store CE Workspace feature layer paths and layer visualizations. This will allow you to reopen the saved project at any time, view the added layers in the Contents pane, and continue working with them.

Start ArcGIS Pro application. Click on *Start without a template* option.

<img src="../../../assets/images/ce-pro/training-01/image1.png" style="width:6.5in;height:1.67569in" alt="A group of icons with text Description automatically generated" />

In the opened window, click on *New Map \> New Map*.

<img src="../../../assets/images/ce-pro/training-01/image2.png" style="width:1.31132in;height:2.24086in" alt="Graphical user interface, application Description automatically generated" />

A new map with basemaps layers will be added to the project. Click on *Project, Save Project*.

<img src="../../../assets/images/ce-pro/training-01/image3.png" style="width:1.48in;height:2.15in" alt="A screenshot of a blue screen Description automatically generated" />

In the new opened dialog, navigate to *C:\CE_Course\CreateWorkspace*

<img src="../../../assets/images/ce-pro/training-01/image4.png" style="width:4.72917in;height:3.09771in" alt="A screenshot of a computer Description automatically generated" />

- If you are using ArcGIS Pro 3.3 version, just type **Project** in Name section.

- If you are using ArcGIS Pro 3.1, or 3.2 version, click on New Item and select Folder

<img src="../../../assets/images/ce-pro/training-01/image5.png" style="width:2.80247in;height:1.75024in" alt="A screenshot of a computer Description automatically generated" />

> Type Project.
>
> <img src="../../../assets/images/ce-pro/training-01/image6.png" style="width:2.21906in;height:0.66676in" alt="A screenshot of a computer Description automatically generated" />
>
> Click on any location to deactivate folder name section, and select this newly created folder.
>
> <img src="../../../assets/images/ce-pro/training-01/image7.png" style="width:1.83359in;height:0.54174in" alt="A blue rectangle with black text Description automatically generated" />

Press *Save* button and it will create all necessary ArcGIS Pro folders and files in this location.

<img src="../../../assets/images/ce-pro/training-01/image8.png" style="width:6.10502in;height:2.81289in" alt="A screenshot of a computer Description automatically generated" />

## Create CE database

Click on **CE RCP** tab and open *Workspace \> Create*.

<img src="../../../assets/images/ce-pro/training-01/image9.png" style="width:1.87526in;height:1.47937in" />

The *Create New Workspace* dialog will appear.

***New workspace path** –* it will be automatically filled based on ArcGIS Pro project location. Leave it as it is.

<img src="../../../assets/images/ce-pro/training-01/image10.png" style="width:6.5in;height:1.09167in" />

***Geodata folder path** -* catalog where geodata are stored. Click on <img src="../../../assets/images/ce-pro/training-01/image11.png" style="width:0.2087in;height:0.2087in" /> *Browse* button and navigate to *C:\CE_Course\Geodata* directory, and select **Vilnius** catalog.

<img src="../../../assets/images/ce-pro/training-01/image12.png" style="width:4.83333in;height:2.98882in" alt="A screenshot of a computer Description automatically generated" />

Press *Select Folder* button.

<img src="../../../assets/images/ce-pro/training-01/image13.png" style="width:6.5in;height:1.91597in" alt="A screenshot of a computer Description automatically generated" />

<u>*Note*:</u> *Projected Coordinate System* is filled automatically and taken from the defined *Elevation grid*. The purpose of this parameter is that the created workspace and geodata would have the same coordinate system.

***Also create Local Scene*** – check to create a second scene for 3D visualization.

<img src="../../../assets/images/ce-pro/training-01/image14.png" style="width:6.5in;height:0.44722in" />

Click *OK* button to create a new workspace. It will create Cellular Expert tables, feature datasets and add the new Cellular Expert workspace to the project. This procedure may take a few seconds to complete.

As the results Workspace folder will be created in the same location as ArcGIS Pro project.

<img src="../../../assets/images/ce-pro/training-01/image15.png" style="width:4.48in;height:2.83in" alt="A screenshot of a computer Description automatically generated" />

This folder contains all necessary information for CE project.

<img src="../../../assets/images/ce-pro/training-01/image16.png" style="width:4.82in;height:3.07in" alt="A screenshot of a computer Description automatically generated" />

Get back to ArcGIS Pro and preview that two tabs were created in ArcGIS Pro view.

<img src="../../../assets/images/ce-pro/training-01/image17.png" style="width:2.10446in;height:0.9793in" alt="A picture containing graphical user interface Description automatically generated" />

- Map_3D is Local Scene where you can work in 3D environment.

- Map is 2D map.

Click on Map view and continue to work with the project.

<img src="../../../assets/images/ce-pro/training-01/image18.png" style="width:2.00028in;height:1.02098in" alt="A picture containing graphical user interface Description automatically generated" />

The created workspace and topograhical data will appear on the Table of Contents. Move elevation.tif raster above Topographic layer, and switch on/off layers above it.

<img src="../../../assets/images/ce-pro/training-01/image19.png" style="width:2.58in;height:1.25in" alt="A screenshot of a computer Description automatically generated" />

<img src="../../../assets/images/ce-pro/training-01/image20.png" style="width:6.5in;height:4.00139in" alt="A screenshot of a map Description automatically generated" />

Adjust added rasters symbology by your requirements. Right click on the layer in Contents and choose Symbology.

<img src="../../../assets/images/ce-pro/training-01/image21.png" style="width:3.21in;height:3.42in" alt="A screenshot of a computer Description automatically generated" />

<img src="../../../assets/images/ce-pro/training-01/image22.png" style="width:6.5in;height:4.08264in" alt="A screenshot of a map Description automatically generated" />

# Profile

Go to CE RCP tab, and open *Profile* tool. Here enter:

For Transmitter:

Latitude: 54.7539217

Longitude: 25.2326465

For Receiver

Latitude: 54.7461165\
Longitude: 25.2600037

Then Click on *Manual Profile* button. Preview profile and involved geodata.

Close Profile windows.

# 3D View

Right click on Map_3D and choose New Vertical Tab Group option.

<img src="../../../assets/images/ce-pro/training-01/image23.png" style="width:3.37547in;height:2.63578in" alt="A screenshot of a computer Description automatically generated" />

The project will be split into two windows.

<img src="../../../assets/images/ce-pro/training-01/image24.png" style="width:5.875in;height:3.05864in" alt="A screenshot of a computer Description automatically generated" />

Navigate in the map, 2D and 3D maps will move simultaneously.

Using Explore button switch view angle on the 3D Map.

<img src="../../../assets/images/ce-pro/training-01/image25.png" style="width:0.60425in;height:0.85429in" alt="A screenshot of a phone Description automatically generated" />

<img src="../../../assets/images/ce-pro/training-01/image26.png" style="width:6.5in;height:3.55556in" alt="A screenshot of a computer screen Description automatically generated" />

3D buildings can be added and visualized in Map_3D scene, as an example OpenStreetMap Buildings data can be added from LivingAtlas to the project.

<img src="../../../assets/images/ce-pro/training-01/image27.png" style="width:4.64in;height:2.75in" alt="A screenshot of a computer Description automatically generated" />

<img src="../../../assets/images/ce-pro/training-01/image28.png" style="width:6.5in;height:3.39236in" alt="A screenshot of a computer Description automatically generated" />
