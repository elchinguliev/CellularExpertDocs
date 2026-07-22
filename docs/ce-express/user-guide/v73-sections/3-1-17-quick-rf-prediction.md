# 3.1.17 Quick RF Prediction

Click this button ![icon](../../../assets/images/ce-express/user-guide-v73/p150-img2.png) to open Quic RF Prediction tool.
The Quick RF Prediction is a tool that lets you select a point on the map and make a prediction without the
need to create a cell. [Quick prediction](#kw:quick-rf-prediction:ce-express-rf-prediction) also lets you select a cell as the point, meaning that you can also
make quick predictions with the created cells. The Quick RF Prediction tool calculates only the field strength

![Image p150](../../../assets/images/ce-express/user-guide-v73/p150-img1.png)

![Image p150](../../../assets/images/ce-express/user-guide-v73/p150-img3.png)
coverage.
- To select a cell, hold the CTRL key and click to snap to the required cell. Snapped cells will be
visible in the dialog.

- To predict a preferred location without a cell, define the exact coordinates in the X/Y fields or click
on the map to fill the coordinate fields automatically.
Calculation settings
Resolution
Prediction raster cell size in meters.
Close previous results
If this option is enabled, clicking elsewhere on the map or changing the calculation parameters will close
the previous result raster and open the new one. If disabled, the old calculation raster stays displayed on

![Image p151](../../../assets/images/ce-express/user-guide-v73/p151-img1.png)
the map.
Prediction model
Prediction models that will be used in the prediction calculations.
Cell template
If a snapped cell does not have all the required parameters or no cell is snapped, the parameters will be
taken from the template.

Cell
| Parameter | Description |
|---|---|
| Snapped feature (optional) | A cell from which the calculation will be done. |
| X | X coordinate of the Cell. |
| Y | Y coordinate of the Cell. |
| Height | Cell height above the ground in meters. |
| Azimuth | Cell direction from the North in degrees. |
| Downtilt | Cells vertical angle offset. |
| El. Downtilt | Electrical downtilt value for the cell, in degrees. |
| Antenna | Antenna that will be used in the prediction calculations. |
| Frequency | Frequency value in MHz. |
| Bandwidth | Value in MHz. Required for 4G and 5G technologies. For other technologies define the value as 0.015. |
| Power | Power value in dBm. |
| Misc. loss | Miscellaneous loss value in dB. |
| TX mimo | Transmitter antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64. |
Subcarrier spacing
Value in kHz. Required for 4G and 5G technologies. For other technologies define value 15.
Click on the map to start the calculation. The results will be loaded automatically in the Map view and will
be added to the Layer list tool.
Results:
- Field Strength raster in dBm.
