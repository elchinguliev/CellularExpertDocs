# Line of Sight (Profile)

## Modelling Outdoor Coverage

The CE tools make use of three distinct GIS data layers to obtain high precision modelling of radio wave propagation losses:

1. **Digital Terrain Model** (DTM), also known as Digital Elevation Model (DEM), which describes Earth surface, i.e., path terrain profile in terms of ground elevation above uniform sea level.
2. **Obstacles layer**, delineating buildings and other such objects above Earth surface that may be considered to be principal impediments for radio wave propagation.
3. **Clutter layer**, delineating natural occurring or human cultivated ground cover that may be partially penetrable by radio waves, such as natural vegetation (e.g., forests, trees, bushes) or various crops, gardens, parks, etc.

![DSM diagram — DTM, clutter losses, and obstacles combine into the Digital Surface Model](../../assets/images/ce-pro/training-05/p002-img25.png)

![CE Pro map view and calculated profile chart showing Elevation, Buildings, Clutter, Profile, and Fresnel zones](../../assets/images/ce-pro/training-05/p002-img24.png)

## Point to Point (Profile) Input

- Geodata
  - Elevation
  - Buildings
  - Clutter
- Frequency
- Fresnel zone (%)
- Earth radius
- Transmitter
  - Height
  - Power
- Receiver
  - Height
  - Power

![Point to point profile input — map view with a dashed profile line between two points](../../assets/images/ce-pro/training-05/p003-img1.png)

## Profile Calculations

- General
  - Clearance
  - Clearance Percentage
  - Clearance Distance
  - Distance to NLOS
  - Distance to OLOS
- Power Budget
  - Downlink FS
  - Uplink FS
  - FWA downlink RSL
  - FWA uplink RSL
- Path Loss
  - Total Path Loss
    - Model Loss
    - Diffraction Loss
    - Penetration Loss
    - Receiver Clutter Loss
    - Clutter Loss
- Angles

![Calculated Profile chart with General Calculations, Power Budget, Path Loss, and Angles results](../../assets/images/ce-pro/training-05/p004-img4.png)

## Dynamic Profile

- Fix transmitter
- Dynamic option

![Dynamic profile — map view with Earth Curvature profile chart showing Tx, Rx, Profile, LOS, Fresnel (Primary), Fresnel (60% Clearance), and Lowest Clearance](../../assets/images/ce-pro/training-05/p005-img1.png)

## Profile Symbology

- Define colors for each object in profile

![Profile symbology — color picker for elements displayed in the profile chart](../../assets/images/ce-pro/training-05/p006-img1.png)

## Profile 3D

![CE Express Antennas panel with 3D map view and calculated profile chart](../../assets/images/ce-pro/training-05/p007-img1.png)

![CE Express 3D view of mmWave cells with calculated profile chart](../../assets/images/ce-pro/training-05/p007-img2.png)

![CE Express Layers panel with 3D building view and calculated profile chart](../../assets/images/ce-pro/training-05/p008-img1.png)

![CE Express 3D view of mmWave site with calculated profile chart](../../assets/images/ce-pro/training-05/p008-img2.png)

## Visibility Prediction Input

- Geodata
  - Elevation
  - Obstacle
- Frequency
- Calculation radius
- Earth radius
- Transmitter
- Receiver (height)

![Visibility Prediction calculation settings panel with map view of selected cells](../../assets/images/ce-pro/training-05/p009-img2.png)

![Map view showing four selected cell sites for visibility prediction](../../assets/images/ce-pro/training-05/p009-img1.png)

## Visibility Results

- Line of Sight
- Required height for LoS
- Clearance

![Visibility results map with Minimum Receiver Height, Line of Sight, Clearance, and Best Server legend](../../assets/images/ce-pro/training-05/p010-img1.png)

![Visibility results map showing minimum receiver height values around cell sites](../../assets/images/ce-pro/training-05/p010-img2.png)

## Visibility: Line of Sight

Possible values:

- 0
- 1

![Line of Sight visibility result — green area indicates LOS value 1](../../assets/images/ce-pro/training-05/p011-img1.png)

## Visibility: Clearance

- Clearance – clearance of visibility line between Tx to Rx as a distance in meters

![Clearance diagram — visibility line passes 6.5 m above the highest obstacle](../../assets/images/ce-pro/training-05/p012-img3.png)

![Clearance result map with Not Visible, -1 - 1, and Visible legend](../../assets/images/ce-pro/training-05/p012-img1.png)

## Visibility: Minimum Receiver Height

- Receiver height – calculate required receiver heights to have a visibility

![Minimum receiver height result map with Lower than 2 m, 2 m - 10 m, 10 m - 50 m, and More than 50 m legend](../../assets/images/ce-pro/training-05/p013-img1.png)

## Visibility: Line of Sight Sum Meter Topo Data

![Visibility comparison using 0.2 m and 1 m topo data — rural terrain example](../../assets/images/ce-pro/training-05/p014-img1.png)

![Visibility comparison using 0.2 m and 1 m topo data — urban building example with zoomed detail](../../assets/images/ce-pro/training-05/p014-img2.png)

## Surface vs Elevation+Obstacles

![Surface grid vs Elevation+Obstacles grid diagram — Tx/Rx visibility compared against DSM, obstacles, and elevation](../../assets/images/ce-pro/training-05/p015-img3.png)

![Visibility result using Surface grid — obstructed areas shown in red](../../assets/images/ce-pro/training-05/p015-img1.png)

![Visibility result using Elevation + Obstacles grid — visible areas shown in green](../../assets/images/ce-pro/training-05/p015-img2.png)

## Surface

![Profile using the Surface grid — General calculations and FWA power budget for an mmWave cell](../../assets/images/ce-pro/training-05/p016-img1.png)

## DTM + Obstacles (Buildings/Vegetation)

![Profile using DTM + Obstacles grid — General calculations and FWA power budget for an mmWave cell](../../assets/images/ce-pro/training-05/p017-img1.png)

## DTM + Buildings + Vegetation

![Profile using DTM + Buildings + Vegetation grid — General calculations and FWA power budget for an mmWave cell](../../assets/images/ce-pro/training-05/p018-img1.png)
