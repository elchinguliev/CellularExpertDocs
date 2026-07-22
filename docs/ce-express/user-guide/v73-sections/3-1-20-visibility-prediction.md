# 3.1.20 Visibility prediction

Click this button to open Visibility prediction tool.
Visibility calculations refer to the determination of line-of-sight between transmitting and receiving antennas,

![Image p170](../../../assets/images/ce-express/user-guide-v73/p170-img1.png)

![Image p170](../../../assets/images/ce-express/user-guide-v73/p170-img2.png)
assessing whether any obstructions might impede direct signal transmission.
Calculation name
Name of the calculation that will be displayed in the Prediction history.
Resolution
Prediction raster cell size in meters.

| Parameter | Description |
|---|---|
| Max radius | Maximum calculation radius in kilometers. |
| Receiver height | Receiver height above the receiver reference height selected in the workspace settings. |
| Effective earth radius | Earth radius was used for the calculations. |
| Layer to calculate | All selected layers on which predictions can be performed. |
Template
A template which corresponds to the selected layers. When the layer changes the templates change as
well.
Visibility Prediction is a tool that calculates 4 different results:
- Clearance, m – the distance from the profile that is covered or is not covered.
- Line of Sight (LOS) – confirms whether visibility exists between the receiver and transmitter with
the provided receiver height.
- Best Server – the same calculation as for RF Prediction.
