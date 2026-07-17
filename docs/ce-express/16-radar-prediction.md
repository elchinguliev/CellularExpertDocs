# Radar Prediction

> **Version:** CE Express v7.3

Radar Prediction calculates the detection reach of radar signals. Detection range varies by target type — drones are identified within a shorter distance than aircraft.

---

3.1.24 Radar prediction
Click this button to open Radar prediction tool.
Radar Prediction is a tool that lets you calculate predictions on radars. Depending on the view angle and
the size of the radar, Radar Predictions will show the reach of radar signals.
Calculation settings
Calculation name
Name of the calculation that will be displayed in Prediction history.
Resolution
Prediction raster cell size in meters.
Best server count
Option to calculate up to 5 best servers.
Radar template
If the radar misses the required parameters, the parameters from the template will be used.
Target cross-section, m^2
This parameter describes the target size in square meters.
Selected
Current amount of selected radars.
Results:
• Field Strength raster in dBm

3.1.25 Network availability
Click this button to open Network availability tool.
This tool is designed to check if coverage exists at a chosen location. Define the exact coordinates in the
dialog or click on the map to fill the coordinate fields automatically and the tool automatically provides the
information about possible networks at this location.
The location can be defined manually in the X/Y fields or by clicking on the map. As a result, detailed
information about possible connections is displayed:
• Cell name – cell identification.
• Signal strength – signal value in dBm.
• Azimuth – direction from Receiver to Transmitter.
• Distance – distance between Transmitter and Receiver.
• CPE count – cpe count in a cell.
• CPE throughput – total cpe throughput in a cell.
• Calculate profile – option to open a detailed profile between Transmitter and Receiver.
In addition, the lines between Transmitter and Receiver are displayed on the map.

The lines on the map can be visualized in different ways. Move the mouse cursor on the calculate profile
button in tabular view.
Then the appropriate line will be visualized differently.

It is possible to draw a profile from the provided results. Press the Calculate profile button to open the
profile.
3.1.26 Model Tuning
Click this button to open Model tuning tool.
Model Tuning is a tool to optimize prediction model parameters based on test points. These test points

must be bound to cells by their cell id.
Calculation Name
Name of the calculation that will be displayed in the Prediction history.
Resolution
Prediction raster cell size in meters.
Prediction model
Select which model will be tuned.
Use the Features tool to select measurements.
Selected
The count of selected measurement points.
Cell to use
Select the Cell with which you want to do the drive test. At the moment, measuring for a single cell is
supported.
Press Calculate to initiate the model tuning. The model tuning task will be added to the Prediction History
dialog.
