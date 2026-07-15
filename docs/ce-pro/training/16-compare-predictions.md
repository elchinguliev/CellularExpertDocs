# Compare Predictions

> **Version:** CE Pro v4.9

### 9.8 Compare Predictions
Compare Predictions is a tool that lets you compare the results of RF predictions with different parameters.
There are 4 possible parameters to choose from: Antenna, Azimuth, Tilt, and Height. When a different
parameter is selected, the selected parameter settings dialog also changes. This tool is extremely useful if
the user wants to quickly check which parameter creates the best possible prediction coverage.
Click the button to open the Compare Prediction dialogue.
Selected Cell
The cell on which the predictions will be performed
Cell Templates
Cell Templates will be used in the prediction calculations.
Resolution
Cell size in meters
Parameters

A list of 4 parameters: Antenna, Azimuth, Tilt, and Height. Select one of the parameters to execute the
predictions.
Current Parameter
The parameter that is currently present in the cell.
Minimal Signal Strength
Signal strength is the floor of the predictions. No signal lower than this value will be included in the
calculations.
From
The starting value of the parameter for calculations
To
The destination value of the parameter for calculations
Step
The increment by which the starting point will reach the destination
Run Calculation
Starts the prediction calculation.
If the user selects one of the results from the results table, that result will be highlighted in the bar chart as
well as the corresponding prediction layer on the map.
Compare Predictions also provides the possibility to create a Difference Raster – a raster that is made
from two RF Prediction rasters that shows the value differences between them. If the user wants to apply
the parameter that produces the biggest coverage value, he can select one of the results from the result
table and press Apply Parameters.

Apply Parameters
Applies the selected parameter to the currently selected cell.
Create Difference Raster
Creates a raster that is made from two RF Prediction rasters. It shows the value differences between them.


### 9.9 Optimal Site Positions
Optimal Site Positions is a tool that lets the user find optimal positions for a site based on specified
parameters. The prediction produces two rasters:
• Covered Points – defines what number of points are covered in a certain pixel
• Coverage Percentage – the percentage by which the pixel is covered. Meaning that 100% is a fully
covered point
Click the button to open the Optimal Site Positions dialogue.

Calculation Name
The name of the current calculation.
Resolution
Cell size in meters.
Candidate Points
The CE layers contain network objects.
Selected Model
The prediction model list.
Tower height
The height of the tower that hosts the site.
Frequency
The frequency value in MHz.
TX power
Transmitter power in dBm.
TX antenna gain
Transmitter gain in dBi.
RX antenna gain
Receiver antenna gain in dBi.
RX sensitivity
Receiver sensitivity in dBm.
Path loss cutoff
The path loss is the floor of the prediction. No path loss lower than this value will be included in the
calculations.
Run Calculation
Starts the prediction calculation.

Results:
• Covered Points
• Coverage Percentage


### 9.10 View Statistics
View Statistics is a tool that calculates the total coverage of a polygon based on its overall coverage (signal
strength, dl throughput, etc.).
The resulting statistics include the total coverage and individual coverage of each polygon segment.
Click the button to open the View Statistics dialogue. To Add Statistics, press the “Add Statistics”
tab on the dockpane.

#### 9.10.1 Statistics
When the calculation is complete, you will be redirected to the Statistics window where you can view the
calculation results. The immediate expander of the calculation shows the overall coverage (in percentages)
of all the polygon regions.
By opening the expander, you can examine the specific regions, their population, and area coverages.
You can also change the colors of the color bands by clicking the squares near the region values.

Table button
View the details about the polygon areas and calculated data in a table. Also, export the table data in CSV
format.

The button lets you edit the selected statistic.
To exit edit mode and cancel all changes, click the Exit Edit Mode button.


#### 9.10.2 Add Statistics
Add Statistic Parameters
Statistic Name
The name of the Statistic.
Raster
The raster layer of one of the coverage results.
Polygon Layer
The polygon layer of which the coverage will be calculated.
Point Layer (Optional)
Used to specify the calculation.
Name Field
Defines the names of territories that will be displayed in the results.
Population Field (Optional)

Establishes the population field that will be used to calculate the total coverage of the population.
Color Bands
The color of each segment in the statistics. The color bands are automatically retrieved from the raster layer
if it contains symbolization.
+
Add a new color band
X
Remove color band
Run
Run the statistics calculation.

### 9.11 Network Manager
Network Manager is a tool that lets you group cells and repeaters into networks based on their frequency
groups and technologies. In doing so, you can easily select particular networks and do RF Calculations
on them without needing to select any particular network objects. The technologies are taken from the Cells
table.
Network Manager tracks the changes in the technology and frequency_group fields of Cells and Repeaters
tables. If the values of these fields should change, the network manager will accommodate such changes
by regrouping changed parameters based on the new technologies and frequency groups.
When frequency groups are modified, removed, added, or affected in any other way, the frequency group
titles will change color from green to red. While the RF calculation is processing the title color will change
to yellow. When the RF calculation is completed on that frequency group, the current network configuration
is saved, and the title color changes back to green.
Click the button to open the Network Manager dialogue. To create a network, press the “+” button
on the dockpane.
Add Network Parameters
Name
The name of the network

Technology
The technology that the network will be based on. All network objects will be filtered by it in the network.
Create Network
Add network to the network list.
Network Manager Parameters
Frequency Groups
Frequency groups that share the same technology.
Last Calculated
The last time the calculation was started
Calculation Status
Status of the current calculation
Selected Frequency Groups
Frequency groups on which the RF Calculations will be completed.
Features in Network
Number of Network objects that are present in the Selected Frequency Groups.
Uncalculated Features
Number of Network objects that have not yet been added to an RF calculation.

+
Adds frequency group to Selected Frequency Groups.
X (inside the network)
Removes frequency group from Selected Frequency Groups.
X (in the network title)
Removes network from the network list.
Calculate
Opens the RF calculation dialog with the selected network objects
