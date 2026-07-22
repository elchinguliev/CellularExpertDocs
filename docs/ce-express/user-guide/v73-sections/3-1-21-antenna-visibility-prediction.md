# 3.1.21 Antenna visibility prediction

Click this button to open Antenna visibility prediction tool.
The Antenna Visibility prediction tool is designed to calculate and visualize the feature’s Line-of-sight

![Image p171](../../../assets/images/ce-express/user-guide-v73/p171-img1.png)

![Image p171](../../../assets/images/ce-express/user-guide-v73/p171-img2.png)
clearance for features based on their azimuth, tilt and selected antenna pattern.

| Parameter | Description |
|---|---|
| Calculation Name | Name of the calculation that will be displayed in Prediction history. |
| Resolution | Prediction raster cell size in meters. |
| Cell template | If the cell is missing the required parameters, the parameters from the template will be used. |
| Attenuation threshold, db | Maximum allowable signal loss for determining effective signal visibility. |
Results:
- Line of Sight (LOS) clearance – height difference between the receiver point and feature’s straight
line-of-sight based on tilt and azimuth.
- Pattern clearance – Height difference between the receiver point and the lowest point of the
antenna pattern that’s above the set threshold.
