# Visibility Prediction

> **Version:** CE Pro v4.9

### 9.7 Visibility Prediction
Visibility calculations refer to the determination of line-of-sight between transmitting and receiving antennas,
assessing whether any obstructions might impede direct signal transmission.
Visibility Prediction is a tool that calculates 4 different results:
• Minimum Receiver Height – the minimum height of a receiver that could be visible to the transmitter
• Line of Sight – confirms whether visibility exists between the receiver and transmitter with the
provided receiver height
• Clearance Height – the distance from the profile that is covered or is not covered.
• Best Server – the same calculation as for RF Prediction
Click the button to open the Visibility Prediction dialogue.

Resolution
Cell size in meters
Max Radius
The maximum radius of the prediction
Receiver height
Receiver height above the ground.
Effective Earth Radius
Earth radius in kilometers, used for the calculations.
Layers to calculate
All present CE layers on which predictions can be performed
Template
A template that corresponds to the selected layers. When the layer changes the templates change as well.
Selected
Network objects that are present on the selected network layer. The visibility prediction will be performed
on all of them.
Run Calculations
Starts the prediction calculation.

Results:
• Minimum Receiver Height in meters
• Line of Sight – either visible (1) by the network objects or not (0)
• Clearance in meters

• Best Server
