**Cellular Expert**

**4. Cell Prediction Exercise**

**\**

# Objective

Explain and show the main parameters for Cell object and how they influence calculations.

At the end of exercise you will be able to:

- Get familiar with main parameters of the cell.

- How geodata is included in the predictions.

- Manage and edit data.

# Initial data

Prepared project with:

- Network objects.

- Geodata.

- Equipment and models.

<img src="../../../assets/images/ce-pro/training-04/image1.png" style="width:6.5in;height:3.48542in" alt="A screenshot of a map Description automatically generated" />

# Cell Parameters

## Network object parameters

Open ArcGIS Pro project from C:\CE_Course\CellPrediction\Project catalog, name Project.aprx.

To perform a Cell prediction, the tool retrieves the necessary parameters from the database to calculate signal strength and other prediction layers. Locate Cell NBa 02 using the cell name parameter and select it on the map. Then, open the Object Editor tool. <img src="../../../assets/images/ce-pro/training-04/image3c.png" style="width:0.29071in;height:0.49421in" />

<img src="../../../assets/images/ce-pro/training-04/image3.png" style="width:6.5in;height:1.96875in" alt="A screenshot of a computer screen Description automatically generated" />

Double-click on the cell object in Object Editor to display its parameters. Preview them one by one to get better understanding of available parameters in Cellular Expert.

<img src="../../../assets/images/ce-pro/training-04/image4.png" style="width:2.85079in;height:4.27012in" alt="A screenshot of a computer Description automatically generated" /> <img src="../../../assets/images/ce-pro/training-04/image5.png" style="width:2.86458in;height:4.28161in" alt="A screenshot of a computer Description automatically generated" />

Close Object Editor tool.

# Cell Area Predictions

To estimate expected cell coverage without topographical data, we can use Calculate Cells Area tool. It will take several parameters from Cell object:

- Prediction model radius.

- Antenna 3dB level patterns.

It helps very quickly estimate antenna or antennas coverage without topographical data.

Make sure that NBa 02 cell is selected and Calculate Cell Area tool.

<img src="../../../assets/images/ce-pro/training-04/image6.png" style="width:4.49021in;height:1.15641in" alt="A white rectangular object with a black border Description automatically generated" />

Press Run Calculations and the tool will provide you a feature class layer in the map view.

<img src="../../../assets/images/ce-pro/training-04/image7.png" style="width:5.91in;height:3.7in" alt="A screenshot of a computer Description automatically generated" />

Close Calculate Cell Area tool and disable NBa 02 Servitude results in the Contents.

<img src="../../../assets/images/ce-pro/training-04/image8.png" style="width:4.1985in;height:0.77094in" alt="A blue rectangle with a white background Description automatically generated" />

# Quick prediction

The tool allows for calculations without altering any parameters in the database and is designed specifically for evaluating "what if" scenarios. The prediction output is a signal strength raster in dBm, which considers all necessary parameters such as cell properties, antenna specifications, the prediction model, and topographical data.

Open Quick Prediction tool. Move mouse cursor on top of selected Cell and click on it to snap it.

<img src="../../../assets/images/ce-pro/training-04/image9.png" style="width:2.6in;height:1.85in" alt="A screenshot of a video game map Description automatically generated" />

Coordinates and other parameters will be taken from snapped Cell.

<img src="../../../assets/images/ce-pro/training-04/image10.png" style="width:3.19in;height:2.43in" alt="A screenshot of a cell phone Description automatically generated" />

Change resolution from 10 to 2, run predictions and preview results.

<img src="../../../assets/images/ce-pro/training-04/image11.png" style="width:6.5in;height:3.35764in" alt="A map with colorful spots Description automatically generated with medium confidence" />Change Azimuth from 357 to 50 in Quick prediction tool and run predictions.

Compare predictions.

<img src="../../../assets/images/ce-pro/training-04/image12.png" style="width:6.5in;height:3.40069in" alt="A map with colorful spots Description automatically generated with medium confidence" />Run several more predictions by changing the parameter. Change parameters one by one and run RF predictions for each new parameter defined in the table below.

| **Parameter name**  |                         **Value** |
|---------------------|----------------------------------:|
| Height above ground |                                35 |
| Downtilt            |                                 2 |
| Tx MIMO             |                                 8 |
| Power               |                                45 |
| Antenna             | ObjectID: 451, Alpha Wireless Ltd |
| Frequency           |                              1800 |

# RF Prediction

The RF Prediction tool is designed to simultaneously calculate multiple cells and provide overall coverage for all selected objects. It also performs additional calculations, including best server, interference, and throughput analyses.

Select NBe 02 cell on the map.

<img src="../../../assets/images/ce-pro/training-04/image13.png" style="width:4.71in;height:3.38in" alt="A map of a city Description automatically generated" />

Open RF Prediction tool and run calculations with the same parameters as defined in the picture below.

<img src="../../../assets/images/ce-pro/training-04/image14.png" style="width:3.93in;height:2.82in" alt="A screenshot of a computer Description automatically generated" />

Preview results are loaded in the Contents and visible on the map. The meaning of each prediction rasters will be covered in 5G Prediction exercise.

<img src="../../../assets/images/ce-pro/training-04/image15.png" style="width:1.82in;height:3.11in" alt="A screenshot of a computer Description automatically generated" />

Turn off Best Server 1, so only Field Strength 1 raster will be visible on the map.

<img src="../../../assets/images/ce-pro/training-04/image16.png" style="width:6.5in;height:3.69583in" alt="A screenshot of a computer screen Description automatically generated" />

Right click on Field Strength 1 raster and choose Symbology. Define colors and thresholds the same as in the picture below:

<img src="../../../assets/images/ce-pro/training-04/image17.png" style="width:3.89in;height:2.17in" alt="A screenshot of a computer Description automatically generated" />

Then leave Field Strength 1 selected in Contents

<img src="../../../assets/images/ce-pro/training-04/image18.png" style="width:1.7815in;height:0.56258in" alt="A blue rectangle with black text Description automatically generated" />

Open Raster Layer, and change Transparency to 50.

<img src="../../../assets/images/ce-pro/training-04/image19.png" style="width:2.13572in;height:0.35422in" />

Field Strength raster looks like this one.

<img src="../../../assets/images/ce-pro/training-04/image20.png" style="width:6.5in;height:3.16389in" alt="A screenshot of a computer screen Description automatically generated" />

Close Symbology tool.

Blue, yellow color shows lower signal strength values. Open Profile tool and do a profile from NBe 02 Cell to these areas. Use fixed transmitter option to quickly change the receiver point.

<img src="../../../assets/images/ce-pro/training-04/image21.png" style="width:6.5in;height:2.97639in" alt="A screenshot of a computer Description automatically generated" />

Close Profile windows.

## Antenna

To include different parameters in RF Predictions, you'll need to update those parameters for the cell in the database. This can be done using the dedicated graphical interface, Object Editor, or by directly modifying the parameter in the table.

Turn off prediction results. Open Object Editor for the same selected Cell. Double click on NBe 02 cell.

<img src="../../../assets/images/ce-pro/training-04/image22.png" style="width:3.92in;height:1.14in" alt="A screenshot of a computer Description automatically generated" />

Find antenna parameters. Click on Model field to filter the antennas.

<img src="../../../assets/images/ce-pro/training-04/image23.png" style="width:3.91in;height:0.93in" alt="A screenshot of a computer Description automatically generated" />

Here type Telrad and it will automatically provide the list with defined letters.

<img src="../../../assets/images/ce-pro/training-04/image24.png" style="width:4.29227in;height:1.13558in" alt="A screenshot of a computer Description automatically generated" />

Double click on Telrad_3GHz_panel_antenna antenna to define it for the cell.

<img src="../../../assets/images/ce-pro/training-04/image25.png" style="width:4.13599in;height:1.04181in" alt="A screen shot of a computer Description automatically generated" />

Before defining the antenna, you can press View Antenna button <img src="../../../assets/images/ce-pro/training-04/image26.png" style="width:1.04181in;height:0.30213in" /> to open Antenna Viewer dialog. It will open the assigned antenna pattern visualization, you can also find and preview another antennas here.

<img src="../../../assets/images/ce-pro/training-04/image27.png" style="width:6.5in;height:1.34792in" alt="A screen shot of a screen Description automatically generated" />

Close Antenna Viewer dialog, and press Save Changes button.

Run RF Predictions with the same settings.

<img src="../../../assets/images/ce-pro/training-04/image28.png" style="width:3.92in;height:2.83in" alt="A screenshot of a computer Description automatically generated" />

Turn off newly loaded Best Server 1 layer, and right click on newly loaded Field Strength 1 layer and choose Symbology.

Expand Options and choose Import from layer.

<img src="../../../assets/images/ce-pro/training-04/image29.png" style="width:3.89in;height:1.18in" alt="A screenshot of a computer Description automatically generated" />

For Symbology layer choose firstly calculated Field Strength layer.

<img src="../../../assets/images/ce-pro/training-04/image30.png" style="width:3.91in;height:4.63in" alt="A screenshot of a computer Description automatically generated" />

Run symbology conversion. It will apply the same symbology as a first field strength layer.

Compare both results.

# Compare predictions

To compare predictions, users can utilize the functionality created by CE or use GIS tools, such as Raster Calculator.

Turn off newly calculated prediction layers, open View \> Geoprocessing, and in search line type: Raster Calculator

<img src="../../../assets/images/ce-pro/training-04/image31.png" style="width:3.93in;height:2.2in" />

Open Raster Calculator (Spatial Analyst Tools), and define the formula:

"CE Prediction 2: CE Calculation\5G\3500\Field Strength 1" - "CE Prediction 1: CE Calculation\5G\3500\Field Strength 1"

Output path: C:\CE_Course\CellPrediction\Calculations\Difference.tif

<img src="../../../assets/images/ce-pro/training-04/image32.png" style="width:4.79in;height:3.35in" alt="A screenshot of a computer Description automatically generated" />

Preview results, if a value is:

- Positive – the second prediction signal strength value with Telrad antenna is higher.

- Negative - the second prediction signal strength value with Telrad antenna is lower.

Close Geoprocessing window.

# Cell Statistic

Cellular Expert includes its own statistics tools that use polygons to determine overall coverage and coverage for each polygon segment. Coverage analysis by polygon is covered in a separate exercise. Here, we will focus on analyzing coverage for individual points and how to obtain the signal value for each point.

Zoom to s3 site object, which contains three cells: NBc 01, NBc 02 and NBc 03.

<img src="../../../assets/images/ce-pro/training-04/image33.png" style="width:4.33in;height:3.45in" alt="A map of a green area Description automatically generated" />

Open Map \> Add Data and navigate to C:\CE_Course\CellPrediction\Shape.gdb, select Address_points and click OK to add it to the map.

<img src="../../../assets/images/ce-pro/training-04/image34.png" style="width:5.76in;height:3.5in" alt="A map of land with many small green and blue dots Description automatically generated" />

Select NBc 01, NBc 02 and NBc 03 on the map, and run RF Prediction with these settings:

<img src="../../../assets/images/ce-pro/training-04/image35.png" style="width:4.83in;height:2.98in" alt="A screenshot of a computer Description automatically generated" />

Preview loaded results especially Field Strength 1 and Best Server 1 rasters.

Open Geoprocessing tool, in Search line type Extract Multi Values, and open Extract Multi Values to Points tool.

<img src="../../../assets/images/ce-pro/training-04/image36.png" style="width:4.83in;height:1.42in" alt="A screenshot of a computer Description automatically generated" />

Define:

- Input point features: Address_points

- Input rasters: Currently calculated Field Strength 1, Best Server 1, Field Strength 2, and Best Server 2 rasters.

<img src="../../../assets/images/ce-pro/training-04/image37.png" style="width:4.8in;height:2.84in" alt="A screenshot of a computer Description automatically generated" />

Press Run.

Turn off prediction layers, then right click on Address_points layer and click on Attribute Table.

<img src="../../../assets/images/ce-pro/training-04/image38.png" style="width:3.6in;height:2.52in" alt="A screenshot of a computer Description automatically generated" />

Scroll right in the opened table, and preview newly generated values.

<img src="../../../assets/images/ce-pro/training-04/image39.png" style="width:1.31268in;height:2.47951in" alt="A screenshot of a white grid with numbers Description automatically generated" />

Click on Select By Attribute, and in the opened tool define as in the picture below.

<img src="../../../assets/images/ce-pro/training-04/image35.png" style="width:3.12071in;height:1.01929in" /><img src="../../../assets/images/ce-pro/training-04/image36.png" style="width:3.04218in;height:1.69521in" alt="A screenshot of a computer Description automatically generated" />

Press Apply button. The tool will select all points with FS1 value greated than -120dBm.

Right click on FS1 field and choose <img src="../../../assets/images/ce-pro/training-04/image37.png" style="width:1.27083in;height:0.19792in" />

<img src="../../../assets/images/ce-pro/training-04/image41.png" style="width:6.5in;height:3.57708in" alt="A screenshot of a computer Description automatically generated" />

Go back to table view, and open Select By Attribute tool again. Define parameters as defined in the picture below.

<img src="../../../assets/images/ce-pro/training-04/image42.png" style="width:4.63in;height:1.51in" alt="A screenshot of a computer Description automatically generated" />

Press OK, the tool will select anly these points which is operated by Cell ID 7 (Cell Name NBc 01), and FS1 value is greater than -120dBm.

Statistics will be updated too.

<img src="../../../assets/images/ce-pro/training-04/image43.png" style="width:6.5in;height:2.39236in" alt="A screenshot of a computer Description automatically generated" />

Close the table.

Points can be symbolized based on field strength values. Right click on Address_points layer and choose Symbology, here define these settings:

Uniques values.

<img src="../../../assets/images/ce-pro/training-04/image44.png" style="width:4.78in;height:1.88in" alt="A screenshot of a computer Description automatically generated" />

Field 1: BS1

<img src="../../../assets/images/ce-pro/training-04/image45.png" style="width:3.33in;height:3.35in" alt="A screenshot of a computer Description automatically generated" />

Preview points on the map.

<img src="../../../assets/images/ce-pro/training-04/image38.png" style="width:5.39074in;height:4.18507in" alt="A map of a city Description automatically generated" />

Then choose Gradeuated Colors.

<img src="../../../assets/images/ce-pro/training-04/image39.png" style="width:4.78in;height:2.04in" alt="A screenshot of a computer Description automatically generated" />

| Field: FS1 | Classes: 4 |
|----|----|
| <img src="../../../assets/images/ce-pro/training-04/image3d.png" style="width:2.65476in;height:1.30208in" /> | <img src="../../../assets/images/ce-pro/training-04/image3e.png" style="width:2.75149in;height:0.74914in" /> |

Define color range:

<img src="../../../assets/images/ce-pro/training-04/image50.png" style="width:5.94875in;height:2.22948in" alt="A screenshot of a computer Description automatically generated" />

Preview on the map.

<img src="../../../assets/images/ce-pro/training-04/image51.png" style="width:6.5in;height:3.55556in" />
