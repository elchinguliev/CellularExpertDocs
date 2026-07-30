
# Objective

Explain and show the main parameters for Cell object and how they influence calculations.

At the end of exercise you will be able to:

- Analyze line-of-sight visibility with profiling tool;

- Perform visibility analysis with visibility tool.

# Initial data

Prepared project with:

- Network objects.

- Geodata.

- Equipment and models.

<img src="../../../assets/images/ce-pro/training-02/image1.png" style="width:6.5in;height:3.37708in" alt="A screenshot of a computer screen Description automatically generated" />

# Profiling

Navigate to C:\CE_Course\LineOfSight\Project and run Project.aprx file to open the prepared project for Profiling exercise.

The profile offers a detailed view of the topographical data between the transmitter and receiver, providing crucial insights into path loss at the receiver location, expected signal strength, angles, and other relevant information. This data is instrumental in making informed decisions regarding equipment, parameters and conditions of LOS, OLOS and NLOS. Additionally, Cellular Expert has incorporated advanced analyses such as antenna height optimization, what-if scenarios including the addition of obstacles, and reflection analysis. In this exercise, we will explore several of these functions in depth.

First, we need to identify the transmitter location. The transmitter point on the profile can be selected directly on the map, or by entering the coordinates in the Profile dialog. Open Profile tool in CE RCP or CE RLP tabs, and locate the NBa 01 cell, move the mouse cursor over it, and you'll notice the mouse icon change as it snaps to the cell.

<img src="../../../assets/images/ce-pro/training-02/image2.png" style="width:3.5in;height:3.78in" />

Click on NBa 01 once and then define receiver point (please select receiver position by your own).

<img src="../../../assets/images/ce-pro/training-02/image3.png" style="width:6.5in;height:2.69583in" alt="A screenshot of a map Description automatically generated" />

Once receiver position is selected, the profile will be generated and visible in your project. You will get a detailed information about LOS, OLOS and NLOS conditions in map view and graph view.

<img src="../../../assets/images/ce-pro/training-02/image4.png" style="width:6.5in;height:2.96111in" alt="A screenshot of a computer Description automatically generated" />

- Green color shows line of sight (LOS) condition.

- Yellow color shows that the path is obstructed by clutter (OLOS).

- Red color shows that the path is obstructed by elevation or buildings (NLOS).

Click on Show Table option to preview calculations.

<img src="../../../assets/images/ce-pro/training-02/image5.png" style="width:1.73958in;height:1.83333in" />

It will open additional view with the calculations of generated profile.

<img src="../../../assets/images/ce-pro/training-02/image6.png" style="width:2.32in;height:4.98in" alt="A white paper with black text Description automatically generated" />

## Adjust Profile parameters

In a what-if scenario, we can modify the profile parameters. These parameters are automatically extracted from the snapped Cell object and populated in the Profile view, where they can be adjusted as needed. Once changes are made, the profile and all associated calculations will be automatically updated.

### Power

Change Power from 40 to 43 value and Downlink Field Strength and FWA downlink RSL will be recalculated automatically.

<img src="../../../assets/images/ce-pro/training-02/image7.png" style="width:5.67788in;height:0.44798in" />

<img src="../../../assets/images/ce-pro/training-02/image8.png" style="width:2.72955in;height:1.06265in" alt="A white background with black text Description automatically generated" />

### Heights

Adjust the Receiver height value from 1.5 meters to any other value.

<img src="../../../assets/images/ce-pro/training-02/image9.png" style="width:1.84401in;height:1.52105in" alt="A screenshot of a computer Description automatically generated" />

You can do this either through the graphical interface or by simply dragging the receiver point up or down in the graph view. Observe how the profile is recalculated in the map view, including the changes in the line colors, graphical interface, and Path Loss calculations.

<img src="../../../assets/images/ce-pro/training-02/image10.png" style="width:6.5in;height:2.96944in" alt="A screenshot of a computer Description automatically generated" />

### Frequency

Change Frequency value from 3500 to 700.

<img src="../../../assets/images/ce-pro/training-02/image11.png" style="width:5.84457in;height:0.47923in" />

Preview Path Loss calculations and how it affected its value.

<img src="../../../assets/images/ce-pro/training-02/image12.png" style="width:2.70871in;height:1.48979in" alt="A white background with black text Description automatically generated" />

## Profiling with fixed transmitter location

Fixing the transmitter location allows for quicker profile drawing across multiple receiver positions. With the transmitter location fixed, there's no need to re-identify it each time a profile is drawn. Simply change the receiver position by clicking on the map.

Enable Fixed Transmitter option.

<img src="../../../assets/images/ce-pro/training-02/image13.png" style="width:5.79247in;height:0.76052in" alt="A white rectangular object with a black border Description automatically generated" />

Transmitter point is fixed, and the receiver point can be defined by click on the map.

<img src="../../../assets/images/ce-pro/training-02/image14.png" style="width:6.5in;height:1.80833in" alt="A screenshot of a computer map Description automatically generated" />

## Dynamic profile

Turn of Fixed Transmitter option.

There's no need to click on the map to set the receiver location. The profile is automatically redrawn based on the mouse's position on the map. However, this continuous redrawing with each mouse movement can be resource intensive for your workstation. Decide which method works best for you: the fixed transmitter tool or the dynamic profile.

Enable Dynamic Profile option

<img src="../../../assets/images/ce-pro/training-02/image15.png" style="width:4.59439in;height:1.34394in" alt="A screenshot of a computer Description automatically generated" />

Then move mouse coursor on the map and profile will be automatically drawn based on the receiver location.

<img src="../../../assets/images/ce-pro/training-02/image16.png" style="width:5.18in;height:2.5in" alt="A map of a city Description automatically generated" />

Uncheck Dynamic profile option.

## Reflections

Analyzing reflections in point-to-point communication, especially in the context of wireless technologies like 5G, is crucial for several reasons:

- Reflections can either reinforce or interfere with the original signal. By analyzing reflections, engineers can predict signal strength variations caused by multipath propagation, ensuring the quality and reliability of the transmitted signal.

- Reflections can cause interference, leading to signal degradation or loss. Understanding how reflections occur helps in designing systems that mitigate interference, improving the overall performance of point-to-point communication links.

- Reflection analysis aids in determining optimal antenna placement and alignment. It helps in identifying potential reflection points, allowing engineers to position antennas to minimize signal interference from reflections and optimize the link's performance.

- Reflection analysis helps in selecting appropriate frequencies and bandwidths for point-to-point links. By understanding the reflection characteristics at different frequencies, engineers can choose frequencies less prone to interference from reflections, optimizing link performance.

- In urban settings with many obstacles, reflections become more complex and impactful. Analyzing reflections helps in planning point-to-point communication systems in such environments, where multiple surfaces can cause reflections affecting the signal quality.

Make sure that your transmitter is NBa 01.

<img src="../../../assets/images/ce-pro/training-02/image17.png" style="width:5.69871in;height:0.47923in" />

Define Receiver coordinates:

- Latitude: 54.7260853

- Longitude: 25.2339780

- Height: 35

<img src="../../../assets/images/ce-pro/training-02/image18.png" style="width:5.91in;height:2.69in" alt="A screenshot of a computer Description automatically generated" />

Click on Tools tab, expand Reflections option and enable Single Reflections.

<img src="../../../assets/images/ce-pro/training-02/image19.png" style="width:4.17588in;height:3.14167in" alt="A screenshot of a computer Description automatically generated" />

Profile will be automatically updated with reflection line.

<img src="../../../assets/images/ce-pro/training-02/image20.png" style="width:6.5in;height:1.47431in" alt="A screen shot of a graph Description automatically generated" />

And preview Reflection calculations:

<img src="../../../assets/images/ce-pro/training-02/image21.png" style="width:2.95875in;height:2.27115in" alt="A white background with black text Description automatically generated" />

Review them, here is several explanations:

- **Grazing angle** refers to an extremely shallow angle of incidence at which an electromagnetic wave or a signal approaches a surface or boundary. It's called "grazing" because the wavefront almost skims or grazes the surface rather than hitting it head-on.

- **Terrain roughness** refers to the irregularity, unevenness, or variability of the Earth's surface features over a profile path. It encompasses a range of natural landscape elements, including hills, valleys, vegetation, buildings, and other obstructions or surface characteristics. It plays a significant role in determining how electromagnetic waves travel through or interact with the environment.

- **Indination** typically refers to the angle of incidence or the angle at which an electromagnetic wave strikes a surface or interface during its propagation between two points.

Change Transmitter or Receiver heights and preview how Receiver point and reflection calculations are changing.

<img src="../../../assets/images/ce-pro/training-02/image22.png" style="width:6.5in;height:1.46111in" alt="A graph with colorful lines Description automatically generated" />

Turn off Single Reflection.

## Adjust Geodata

To quickly estimate how an obstacle might impact the path between the transmitter and receiver, you can use the Adjust tool. This allows you to modify the current elevation, or add and adjust buildings or clutter without altering the existing topographical data. This enables you to quickly preview general calculations, such as clearance, and assess the potential signal level at the receiver location.

Click on Adjust option (near profile Results).

<img src="../../../assets/images/ce-pro/training-02/image23.png" style="width:2.4in;height:2.93in" alt="A screenshot of a computer Description automatically generated" />

Next, click on the profile graph with the left mouse button and, while holding the button down, drag to select the area where a potential building might be located.

<img src="../../../assets/images/ce-pro/training-02/image24.png" style="width:3.36in;height:3.35in" alt="A graph with different colored lines Description automatically generated" />

Then release mouse left button and the area will be selected, and on the right you will get elevation and clutter heights.

Select each row in the table (use CTRL or Shift buttons).

<img src="../../../assets/images/ce-pro/training-02/image25.png" style="width:2.38in;height:2.82in" alt="A screenshot of a computer Description automatically generated" />

If you modify any selected row, the same value will be applied to all other selected rows as well. Enter the value 55 for any row.

<img src="../../../assets/images/ce-pro/training-02/image26.png" style="width:2.34in;height:2.83in" alt="A screenshot of a computer Description automatically generated" />

Press Update Values button, which will update Profile graph.

<img src="../../../assets/images/ce-pro/training-02/image27.png" style="width:6.5in;height:2.98333in" alt="A screenshot of a computer Description automatically generated" />

## Report

Click on Export tab in Profile.

<img src="../../../assets/images/ce-pro/training-02/image28.png" style="width:4.92in;height:2.45in" alt="A screenshot of a login Description automatically generated" />

Define:

- Author: Student Name

- Organization: Company Name

- Report Name: NBa 01 Rx01

- Profile Report File Path: C:\CE_Course\LineOfSight, and define name Report_NBa01

<img src="../../../assets/images/ce-pro/training-02/image29.png" style="width:4.86in;height:2.02in" alt="A screenshot of a computer Description automatically generated" />

Click on Export Profile. The profile will be generated and opened for you automatically.

<img src="../../../assets/images/ce-pro/training-02/image30.png" style="width:6.5in;height:3.12153in" alt="A screenshot of a computer Description automatically generated" />

## Symbology

Back to ArcGIS Pro project and profile view.

You can click on any object symbology legend and change a color.

<img src="../../../assets/images/ce-pro/training-02/image31.png" style="width:2.07in;height:3.26in" alt="A screenshot of a computer Description automatically generated" />

Change colors for several objects.

<img src="../../../assets/images/ce-pro/training-02/image32.png" style="width:6.5in;height:1.45833in" alt="A white screen with colorful lines Description automatically generated" />

Close Profile tool.

# Visibility prediction

Profile tool is dedicated to analyzing point-to-point conditions. Visibility predictions can calculate point-to-area predictions.

Visibility prediction can be used:

- For mmWave bands to ensure Visibility areas. These frequencies are more susceptible to obstacles like buildings, trees, and even atmospheric conditions. Visibility prediction helps anticipate how these obstacles might affect signal propagation.

- Antenna Placement: Predicting visibility aids in optimal antenna placement. Placing antennas where there's a clear line of sight between the transmitter and receiver maximizes signal strength and quality.

- Cost-Efficiency: Understanding visibility patterns helps in cost-effective network deployment. By placing antennas strategically based on visibility predictions, operators can reduce the number of required installations while ensuring optimal coverage.

- 5G networks often utilize beamforming, where signals are concentrated and directed toward specific users. Line-of-sight (LOS) propagation is critical for beamforming to work effectively. Visibility prediction assists in determining the likelihood of LOS conditions between transmitters and receivers.

Find cell name: NBa 02, and select it on the map.

<img src="../../../assets/images/ce-pro/training-02/image33.png" style="width:4.9in;height:4.43in" alt="A map of a city Description automatically generated" />

Select the object on the map and open Visibility prediction tool in CE RCP or CE RLP tabs.

<img src="../../../assets/images/ce-pro/training-02/image34.png" style="width:3.97in;height:3.27in" alt="A screenshot of a computer Description automatically generated" />

Define these parameters:

- Resolution: 2

- Max radius: 3

- Receiver height: 1.5

- Effective earth radius: 6400

- Layer to calculate: Cells

<img src="../../../assets/images/ce-pro/training-02/image35.png" style="width:3.99in;height:3.38in" alt="A screenshot of a computer Description automatically generated" />

Press Run Calculations. After calculations, Visibility results will be loaded to Contents and visible on the map.

<img src="../../../assets/images/ce-pro/training-02/image36.png" style="width:2.01in;height:4.13in" alt="A screenshot of a computer Description automatically generated" />

**Minimum Receiver Height** – the receiver height in meters, which ensure visibility between transmitter and receiver.

**Line of Sight** – Visibility condition, if value 1 – Visible, if value 0 – Not Visible.

**Clearance** – Fresnel zone obstruction in meters, if value is negative – Fresnel zone is obstructed by X meters.

**Best Server** – Cell Identification, which has highest Clearence value.

Preview all results.

Open Profile tool, and draw a profile from NBa 02 Cell to receiver coordinates:

- Latitude: 54.7248800

- Longitude: 25.2387187

<img src="../../../assets/images/ce-pro/training-02/image37.png" style="width:6.5in;height:1.46528in" alt="A screen shot of a graph Description automatically generated" />

The receiver's height is determined using an elevation grid. In the context of Fixed Wireless Access, antennas are typically installed on building rooftops.

Open Workspace \> Properties.

<img src="../../../assets/images/ce-pro/training-02/image38.png" style="width:1.07in;height:1.78in" alt="A screenshot of a computer Description automatically generated" />

Find Receiver Height Reference option and change value to Clutter Height.

<img src="../../../assets/images/ce-pro/training-02/image39.png" style="width:2.66704in;height:0.7501in" alt="A screenshot of a computer Description automatically generated" />

Press OK to close Parameters dialog.

Click on Manual Profile again.

<img src="../../../assets/images/ce-pro/training-02/image40.png" style="width:6.5in;height:1.475in" alt="A screen shot of a graph Description automatically generated" />

The receiver point now is on top of the clutter, adjust receiver height for Line of Sight condition. Close Profile dialogs.

Open Visibility tool. Run Visibility calculations with the same parameters.

<img src="../../../assets/images/ce-pro/training-02/image41.png" style="width:3.58in;height:3.38in" alt="A screenshot of a computer Description automatically generated" />

Compare newly loaded Visibility results with previous ones.

Leave Line of Sight results active for both predictions.

<img src="../../../assets/images/ce-pro/training-02/image42.png" style="width:2.31in;height:2.93in" alt="A screenshot of a computer Description automatically generated" />

Select on 2<sup>nd</sup> result Line of Sight layer and choose Raster Layer tab in the top of the screen.

<img src="../../../assets/images/ce-pro/training-02/image43.png" style="width:2.93791in;height:0.63551in" alt="A screenshot of a computer Description automatically generated" />

Click on Swipe tool, and click and hold left mouse button. Swipe on the map. You can also apply transparency value for both predicition layers. <img src="../../../assets/images/ce-pro/training-02/image44.png" style="width:2.16697in;height:0.33338in" />

<img src="../../../assets/images/ce-pro/training-02/image45.png" style="width:5.76in;height:6.33in" alt="A map of a city Description automatically generated" />
