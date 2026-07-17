# Visibility Prediction

> **Version:** CE Express v7.3

Visibility Prediction calculates line-of-sight between transmitting and receiving antennas, assessing whether obstructions impede direct signal transmission.

---

Max Z
Highest height level, in meters, up to which the prediction is calculated.
Cell template
If the cell is missing the required parameters, the parameters from the template will be used.
Repeater template
If the repeater is missing the required parameters, the parameters from the template will be used.
3.1.20 Visibility prediction
Click this button to open Visibility prediction tool.
Visibility calculations refer to the determination of line-of-sight between transmitting and receiving antennas,
assessing whether any obstructions might impede direct signal transmission.
Calculation name
Name of the calculation that will be displayed in the Prediction history.
Resolution
Prediction raster cell size in meters.

Max radius
Maximum calculation radius in kilometers.
Receiver height
Receiver height above the receiver reference height selected in the workspace settings.
Effective earth radius
Earth radius was used for the calculations.
Layer to calculate
All selected layers on which predictions can be performed.
Template
A template which corresponds to the selected layers. When the layer changes the templates change as
well.
Visibility Prediction is a tool that calculates 4 different results:
• Clearance, m – the distance from the profile that is covered or is not covered.
• Line of Sight (LOS) – confirms whether visibility exists between the receiver and transmitter with
the provided receiver height.
• Best Server – the same calculation as for RF Prediction.
3.1.21 Antenna visibility prediction
Click this button to open Antenna visibility prediction tool.
The Antenna Visibility prediction tool is designed to calculate and visualize the feature’s Line-of-sight
clearance for features based on their azimuth, tilt and selected antenna pattern.

Calculation Name
Name of the calculation that will be displayed in Prediction history.
Resolution
Prediction raster cell size in meters.
Cell template
If the cell is missing the required parameters, the parameters from the template will be used.
Attenuation threshold, db
Maximum allowable signal loss for determining effective signal visibility.
Results:
• Line of Sight (LOS) clearance – height difference between the receiver point and feature’s straight
line-of-sight based on tilt and azimuth.
• Pattern clearance – Height difference between the receiver point and the lowest point of the
antenna pattern that’s above the set threshold.
3.1.22 Minimum receiver height
Click this button to open Minimum receiver height tool.
Calculates the minimum receiver height required to satisfy LOS condition for selected features.

Calculation settings
Calculation name
Name of the calculation that will be displayed in Prediction history.
Resolution
Prediction raster cell size in meters.
Max radius
Maximum calculation radius in kilometers.
Effective earth radius
Earth radius was used for the calculations.
Overlap priority
Value priority in places where multiple feature calculations overlap
• Lowest (Reach at least 1) – minimum value will be used
• Highest (Reach all) – maximum value will be used
Results:
• Minimum receiver height, m - minimum receiver height required to satisfy LOS condition

• Best Server – Object id of the feature which has the value priority in each pixel. E.g.: In the case of
“lowest” priority setting, pixels have the object id of the feature which has the lowest available
minimum receiver height (best visibility).
3.1.23 Quick minimum receiver height
Click this button to open Quick minimum receiver height tool.
Calculates the minimum receiver height required to satisfy LOS condition for a single feature. Feature
parameters are defined in the tool input fields, therefore it may be a theorical feature that does not exist in
the database.

Calculation settings
Resolution
Prediction raster cell size in meters.
Max radius
Maximum calculation radius in kilometers.
Effective earth radius
Earth radius was used for the calculations.
Close previous results
If this option is enabled, clicking elsewhere on the map or changing the calculation parameters will close
the previous result raster and open the new one. If disabled, the old calculation raster stays displayed on
the map.
Feature
X
X coordinate of the Feature.
Y
Y coordinate of the Feature.
Height
Feature height above the ground in meters.
