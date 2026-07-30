**Cellular Expert**

**3. Object Creation**

\
=

# Objective

Explain and show how to create objects from templates and edit them.

At the end of exercise you will be able to:

- Create object templates.

- Create objects from templates.

- Move and duplicate objects

- Edit objects’ parameters.

# Initial data

Prepared project with:

- Geodata.

# Create templates

Open ArcGIS Pro project named Project.aprx, from *C:\CE_Course\ObjectCreation\Project* catalog.

<img src="../../../assets/images/ce-pro/training-03/image1.png" style="width:6.5in;height:3.49236in" />

Open the *Template Manager* tool from the **CE RCP** toolbar to preview existing Cell templates. Templates help you quickly populate parameters, saving time compared to manual entry. The default workspace already includes several templates, which can be modified or deleted as needed. Templates can be used in several tools:

- Add Object – fills all necessary parameters from template to new object.

- Object Editor – changes existing parameters to new ones according to template.

- Import Objects from File – imports parameters from the template if something is missing in text (CSV, XLSX) file.

- Profile – takes a parameters from a template if Tx or Rx point is not snapped to Cell object.

- RF Prediction – uses template parameters if something is missing in the object.

- Link Prediction - uses template parameters if something is missing in the object.

- Radar Prediciton - uses template parameters if something is missing in the object.

- Visibility Prediction - uses template parameters if something is missing in the object.

- Optimal Site Positions - uses template parameters if something is missing in the object.

- Antenna Visibility - uses template parameters if something is missing in the object.

You can also create new templates and customize the parameters to fit your specific requirements.

To create your own template, right-click on Cell Templates and select *Create New*.

<img src="../../../assets/images/ce-pro/training-03/image2.png" style="width:2.78164in;height:0.58341in" />

Create new templates based on the table below. After entering the parameters for each template, click *Save Changes*. Then, right-click on Cell Templates and select *Create New* to begin creating the next template.

<table style="width:95%;">
<colgroup>
<col style="width: 27%" />
<col style="width: 22%" />
<col style="width: 23%" />
<col style="width: 22%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Parameter</strong></th>
<th colspan="3" style="text-align: center;"><strong>Value</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Cell Template Name</td>
<td style="text-align: center;">5G template 3500</td>
<td style="text-align: center;">5G template 900</td>
<td style="text-align: center;">TETRA</td>
</tr>
<tr>
<td>Bandwidth</td>
<td style="text-align: center;">100</td>
<td style="text-align: center;">10</td>
<td style="text-align: center;">0.015</td>
</tr>
<tr>
<td>Noise Figure</td>
<td style="text-align: center;">6</td>
<td style="text-align: center;">5</td>
<td style="text-align: center;">5</td>
</tr>
<tr>
<td>Subcarrier Spacing</td>
<td style="text-align: center;">30</td>
<td style="text-align: center;">15</td>
<td style="text-align: center;">15</td>
</tr>
<tr>
<td>TX MIMO</td>
<td style="text-align: center;">4</td>
<td style="text-align: center;">2</td>
<td style="text-align: center;">1</td>
</tr>
<tr>
<td>RX MIMO</td>
<td style="text-align: center;">4</td>
<td style="text-align: center;">2</td>
<td style="text-align: center;">1</td>
</tr>
<tr>
<td>Active Antenna Effect</td>
<td style="text-align: center;">0</td>
<td style="text-align: center;">0</td>
<td style="text-align: center;">0</td>
</tr>
<tr>
<td>Cell Load</td>
<td style="text-align: center;">30</td>
<td style="text-align: center;">30</td>
<td style="text-align: center;">0</td>
</tr>
<tr>
<td>Antenna ID</td>
<td style="text-align: center;">514</td>
<td style="text-align: center;">54</td>
<td style="text-align: center;">56</td>
</tr>
<tr>
<td>Height</td>
<td style="text-align: center;">30</td>
<td style="text-align: center;">30</td>
<td style="text-align: center;">30</td>
</tr>
<tr>
<td>Frequency</td>
<td style="text-align: center;">3500</td>
<td style="text-align: center;">900</td>
<td style="text-align: center;">390</td>
</tr>
<tr>
<td>Prediction Model ID</td>
<td style="text-align: center;">3</td>
<td style="text-align: center;">3</td>
<td style="text-align: center;">3</td>
</tr>
<tr>
<td>Prediction Model Configuration ID</td>
<td style="text-align: center;">4</td>
<td style="text-align: center;">5</td>
<td style="text-align: center;">11</td>
</tr>
<tr>
<td>Technology</td>
<td style="text-align: center;">5G</td>
<td style="text-align: center;">5G</td>
<td style="text-align: center;">2G</td>
</tr>
<tr>
<td>Frequency Group</td>
<td style="text-align: center;">3500</td>
<td style="text-align: center;">900</td>
<td style="text-align: center;">390</td>
</tr>
<tr>
<td>Carriers</td>
<td style="text-align: center;">[]</td>
<td style="text-align: center;">[]</td>
<td style="text-align: center;">[]</td>
</tr>
<tr>
<td>Downlink Duplex Factor</td>
<td style="text-align: center;">0.6</td>
<td style="text-align: center;">1</td>
<td style="text-align: center;">1</td>
</tr>
<tr>
<td>Tilt</td>
<td style="text-align: center;">0</td>
<td style="text-align: center;">0</td>
<td style="text-align: center;">0</td>
</tr>
<tr>
<td>Duplex Mode</td>
<td style="text-align: center;">TDD</td>
<td style="text-align: center;">FDD</td>
<td style="text-align: center;">FDD</td>
</tr>
<tr>
<td>Power</td>
<td style="text-align: center;">40</td>
<td style="text-align: center;">40</td>
<td style="text-align: center;">43</td>
</tr>
<tr>
<td>Misc Loss</td>
<td style="text-align: center;">0</td>
<td style="text-align: center;">0</td>
<td style="text-align: center;">0</td>
</tr>
<tr>
<td>Electrical_tilt</td>
<td style="text-align: center;">0</td>
<td style="text-align: center;">0</td>
<td style="text-align: center;">0</td>
</tr>
</tbody>
</table>

# Add objects

Add objects tool helps to create objects manually.

## Site object

Open *Add Object* <img src="../../../assets/images/ce-pro/training-03/image3.png" style="width:0.28125in;height:0.41538in" alt="A blue plus sign with black text Description automatically generated" /> tool, expand the dropdown list menu, and choose Sites.

<img src="../../../assets/images/ce-pro/training-03/image4.png" style="width:3.30208in;height:1.4563in" alt="A screenshot of a computer Description automatically generated" />

Define:

- Name: ST01

- Latitude: 54.73962527

- Longitude: 25.18876518

- Height above ground, m: 55

<img src="../../../assets/images/ce-pro/training-03/image5.png" style="width:3.29167in;height:4.08462in" alt="A screenshot of a computer Description automatically generated" />

Press Save Changes. Site object will be created in the project.

<img src="../../../assets/images/ce-pro/training-03/image6.png" style="width:5.66in;height:3.4in" alt="A map of land with a white circle Description automatically generated" />

Click once on the map in any other location, coordinates will be changed according to map click.

<img src="../../../assets/images/ce-pro/training-03/image7.png" style="width:6.5in;height:3.00208in" alt="A map of a neighborhood Description automatically generated" />

Change:

- Name: ST02

- Height above ground, m: 30

Press Save Changes.

Click on the location, which has a building. Height above ground value will be automatically filled based on building height on location.

<img src="../../../assets/images/ce-pro/training-03/image8.png" style="width:5.83in;height:3.43in" alt="A screenshot of a computer Description automatically generated" />

Change Site Name to ST03 and press Save changes.

## Add Cell

Zoom back to first created Site object. Expand the dropdown list menu and choose Cells.

<img src="../../../assets/images/ce-pro/training-03/image9.png" style="width:4.82359in;height:1.28143in" alt="A screenshot of a computer Description automatically generated" />

Click once on the Site object on the map.

<img src="../../../assets/images/ce-pro/training-03/image10.png" style="width:3.72in;height:2.06in" alt="A map of land with a black circle Description automatically generated" />

Click second time to define Cell azimuth.

<img src="../../../assets/images/ce-pro/training-03/image11.png" style="width:3.69792in;height:2.41169in" alt="A map of a video game Description automatically generated" />

The New Cell will appear on the map.

Enter parameters as defined below:

- **Template**: TETRA 400MHz Sector

- **Name**: CellA

- **Azimuth**: 5

- **Height above ground, m**: 55

- **Prediction model**: CEC ITU-R: 15km radius

<img src="../../../assets/images/ce-pro/training-03/image12.png" style="width:3.4in;height:1.73in" alt="A screenshot of a computer Description automatically generated" />

Click Save Changes.

Change only the following parameters in the dialog and click Save Changes:

- **Name**: CellB

- **Azimuth**: 120

Change only the following parameters in the dialog and click Save Changes:

- **Name**: CellC

- **Azimuth**: 240

Now you should see three cells on the map.

<img src="../../../assets/images/ce-pro/training-03/image13.png" style="width:2.67746in;height:1.93777in" alt="A map of a cell Description automatically generated" />

Zoom to the Site, which was created on the building.

<img src="../../../assets/images/ce-pro/training-03/image14.png" style="width:5.19in;height:3.53in" alt="A aerial view of a building Description automatically generated" />

Cell objects do not require Site object. Create several Cell objects at the corner of the building.

<img src="../../../assets/images/ce-pro/training-03/image15.png" style="width:3.2192in;height:3.7401in" alt="A map of a building Description automatically generated" />

If Site object exist on this building, and you would like to assign it for the Cells. Select Site and Cells on the map using Select Feature tool.

Open Object Editor tool.

<img src="../../../assets/images/ce-pro/training-03/image16.png" style="width:3.11502in;height:1.92735in" alt="A screenshot of a computer Description automatically generated" />

You need to apply Site ID value for each Cell.

<img src="../../../assets/images/ce-pro/training-03/image17.png" style="width:1.82292in;height:0.46875in" />

Double-click on the first Cell, and find Site ID parameter.

<img src="../../../assets/images/ce-pro/training-03/image18.png" style="width:4.62565in;height:0.63551in" alt="A blue and white line Description automatically generated with medium confidence" />

Change it depending on Site Object ID in your project.

<img src="../../../assets/images/ce-pro/training-03/image19.png" style="width:2.89624in;height:0.55216in" alt="A blue line on a white background Description automatically generated" />

Press Save Changes button.

Do it for other Cells. Cells will go under Site object.

<img src="../../../assets/images/ce-pro/training-03/image20.png" style="width:3.07335in;height:1.87526in" alt="A screenshot of a computer Description automatically generated" />

Note. You can apply the correct SiteID value in Add Cells tool too. If Cell is created on top of Site (snapped), then it will automatically take Site_ID value.

## Move objects

Open *Object Editor* <img src="../../../assets/images/ce-pro/training-03/image21.png" style="width:0.32582in;height:0.47822in" /> tool. With *Select Features* button <img src="../../../assets/images/ce-pro/training-03/image22.png" style="width:0.3166in;height:0.46686in" /> select previously created site with 3 cells.

<img src="../../../assets/images/ce-pro/training-03/image23.png" style="width:6.5in;height:2.13472in" alt="A screenshot of a computer Description automatically generated" />

Press the **Move Objects** button in the Object Editor dialog.

<img src="../../../assets/images/ce-pro/training-03/image24.png" style="width:2.82331in;height:0.44798in" />

Define:

- Latitude: 54.7389744

- Longitude: 25.1917101

- Height above ground, m: 60

<img src="../../../assets/images/ce-pro/training-03/image25.png" style="width:3.72917in;height:3.23257in" alt="A screenshot of a computer Description automatically generated" />

Press Save Changes. Objects will be moved to another location based on defined coordinates.

Objects can be moved based on selected location. Choose Select Point button <img src="../../../assets/images/ce-pro/training-03/image26.png" style="width:1.57314in;height:0.37505in" />

Click on the map to define Site and Cells location.

<img src="../../../assets/images/ce-pro/training-03/image27.png" style="width:2.64583in;height:3.33091in" alt="A map of a city Description automatically generated" />

Press Save changes to move the site object.

<img src="../../../assets/images/ce-pro/training-03/image28.png" style="width:3.60417in;height:3.1487in" alt="A map of a cell Description automatically generated" />

## Duplicate objects

Click on Duplicate Objects option.

<img src="../../../assets/images/ce-pro/training-03/image29.png" style="width:2.04195in;height:0.2292in" />

The objects can be duplicated in the same way as Moved. You can enter coordinates directly in the dialog, or use Select Point tool to define a location on the map.

<img src="../../../assets/images/ce-pro/training-03/image30.png" style="width:1.36477in;height:0.30213in" />

Once it is selected, click on the map. The potential position and coordinates will be updated. Define Height above the ground, m: 50

Pres Save Changes

<img src="../../../assets/images/ce-pro/training-03/image31.png" style="width:5.125in;height:3.8237in" alt="A map of a land with buildings and roads Description automatically generated" />

## Change object parameters

With Select tool select Duplicated Cells and Site.

<img src="../../../assets/images/ce-pro/training-03/image32.png" style="width:6.5in;height:2.83264in" alt="A screenshot of a computer Description automatically generated" />

Change newly created objects’ parameters.

Double click on CellA – Copy object and define:

- Name: CellA1

- Azimuth: 20

- Power 43

Press Save Changes.

Do it for other cells, and do not forget to press Save Changes when finishing to change a parameters for a object.

- Name:

  - CellB1

  - CellC1

- Azimuth:

  - For CellB1: 135

  - For CellC1: 270

- Power: 43

Close Object Editor tool.

## Change parameters in Attribute table

Select all objects on the map and open Cells attribute table (right click on Cells \> Attribute Table). Find Power field and right click on it, choose Calculate Field.

<img src="../../../assets/images/ce-pro/training-03/image33.png" style="width:2.7in;height:2.18in" alt="A screenshot of a computer Description automatically generated" />

Define value 45.

<img src="../../../assets/images/ce-pro/training-03/image34.png" style="width:4.09432in;height:0.52091in" alt="A white rectangular object with a black stripe Description automatically generated" />

Press OK button to recalculate value.

Preview Power parameter in Object Editor tool.

# Add Microwave Link

Open Add Object tool and choose Link object in drop-down list menu.

<img src="../../../assets/images/ce-pro/training-03/image35.png" style="width:4.07292in;height:1.85221in" alt="A screenshot of a computer Description automatically generated" />

Click once on ST01 site, it will be the transmitter (Site A).

<img src="../../../assets/images/ce-pro/training-03/image36.png" style="width:2.53125in;height:1.42198in" alt="A map of a city Description automatically generated" />

Click second time on ST02 – it will be a receiver (Site B).

<img src="../../../assets/images/ce-pro/training-03/image37.png" style="width:5.56328in;height:2.06279in" alt="A map of a city Description automatically generated" />

The coordinates will be filled according snapped objects.

<img src="../../../assets/images/ce-pro/training-03/image38.png" style="width:2.76in;height:4.63in" alt="A screenshot of a computer Description automatically generated" />

Adjust Height values.

Note. A link can be created on empty locations and does not require Site object. For this case, Site will be created automatically.

Link profile can be generated before creating a new link.

<img src="../../../assets/images/ce-pro/training-03/image39.png" style="width:3.19836in;height:0.50007in" />

It would show detail view from Tx to Rx locations.

<img src="../../../assets/images/ce-pro/training-03/image40.png" style="width:6.5in;height:1.46319in" alt="A screen shot of a graph Description automatically generated" />

Close Profile view.

## Frequency Plan

The frequency plan is used to define frequencies for new Microwave link. A set of available frequencies will be displayed based on selected frequency plan.

<img src="../../../assets/images/ce-pro/training-03/image41.png" style="width:3.57292in;height:3.37137in" alt="A screenshot of a computer Description automatically generated" />

Before it, define that Site A will use Lower frequencies.

<img src="../../../assets/images/ce-pro/training-03/image42.png" style="width:3.91721in;height:0.88554in" alt="A screenshot of a computer Description automatically generated" />

Site B section will be changed automatically to Upper.

Then if MW link will be Duplex or Simplex. If Duplex option is Yes, then it will be duplex link, of No – simplex. Leave value Yes.

Select carriers 1 and 3.

<img src="../../../assets/images/ce-pro/training-03/image43.png" style="width:4.1985in;height:1.57314in" alt="A screenshot of a computer Description automatically generated" />

Change Power for Carrier 3 to 20.

<img src="../../../assets/images/ce-pro/training-03/image44.png" style="width:3.92763in;height:1.29185in" alt="A screenshot of a computer Description automatically generated" />

## Antenna

Parabolic antennas can be defined for Tx and Rx. Preview selected antenna with option View Antenna.

<img src="../../../assets/images/ce-pro/training-03/image45.png" style="width:6.5in;height:2.97847in" alt="A screenshot of a computer Description automatically generated" />

Close Antenna Viewer dialog.

## Equipment

Radio parameters such as bandwidth, power and modulations are defined here. Leave default radio.

## Name

Define Link name:

<img src="../../../assets/images/ce-pro/training-03/image46.png" style="width:4.15683in;height:0.50007in" />

Press Save Changes and new Link object will be created in the project.

<img src="../../../assets/images/ce-pro/training-03/image47.png" style="width:6.5in;height:1.42847in" alt="A map of a city Description automatically generated" />
