# 3.1.27 Optimal placement

Click this button to open Optimal placement tool.
Optimal placement is a tool that lets the user find optimal positions for a site based on specified parameters.

![Image p184](../../../assets/images/ce-express/user-guide-v73/p184-img1.png)

![Image p184](../../../assets/images/ce-express/user-guide-v73/p184-img2.png)

| Parameter | Description |
|---|---|
| Calculation Name | Name of the calculation that will be displayed in the Prediction history. |
| Prediction Model | The prediction model list. |
| Resolution | Prediction raster cell size in meters. |
| CPE templates | If the CPE is missing required parameters, the parameters from the template will be used. |
| Tower height | The height of the tower that hosts the site. |
| Frequency | The frequency value in MHz. |
| TX power | Transmitter power in dBm. |
| TX antenna gain | Transmitter gain in dBi. |

![Image p185](../../../assets/images/ce-express/user-guide-v73/p185-img1.png)

RX antenna gain
Receiver gain in dBi.
RX sensitivity
Receiver gain in dBi.
Path loss cutoff
The path loss is the floor of the prediction.
The prediction produces two rasters:
- Covered Points – defines what number of points are covered in a certain pixel
- Coverage Percentage – the percentage by which the pixel is covered. Meaning that 100% is a fully
covered point
