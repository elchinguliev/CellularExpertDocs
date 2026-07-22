# 3.1.37 Link prediction

Click this button ![icon](../../../assets/images/ce-express/user-guide-v73/p211-img1.png) to open Link prediction tool.
Calculation settings
Calculation Name
Link Prediction identification.
Link Template
The template will fill all empty or not specified fields with default values that are not necessary for

![Image p211](../../../assets/images/ce-express/user-guide-v73/p211-img2.png)
predictions.

Interference
Calculate Interference
If checked will calculate the interference of multiple links.
Use interference radius
If enabled, also allows to specify a certain radius from either link endpoint. Points outside this range will not

![Image p212](../../../assets/images/ce-express/user-guide-v73/p212-img1.png)
be included in the calculation, speeding up the calculation process. If disabled all links will be used in the
calculations.
| Parameter | Description |
|---|---|
| Interference creation limit | The power threshold below which no interference for links will be calculated. |
| Interference analysis limit | The power threshold below which no links with lesser interference will be included in the analysis. |
| Tx/Rx filter discrimination | The ability of filters in a duplex system to effectively separate and prevent interference between Tx and Rx frequencies. No dBm greater than this will be accounted for in the calculation. |

Field Margin
Include Field Margin in Power Budget
If checked, it will take into account the specified field margin for Power Budget calculations.
Thermal Fade Margin
The threshold below which thermal fade will not be calculated
Tropospheric scatter
Calculate Tropospheric Scatter
Enable/Disable this option.
Troposcatter time percentage
Time Percentage in %.

![Image p213](../../../assets/images/ce-express/user-guide-v73/p213-img1.png)

![Image p213](../../../assets/images/ce-express/user-guide-v73/p213-img2.png)

Method
The standard used to calculate the performance metric.
Statistics
A selection indicating if the metric is calculated based on yearly data or the data from the month with the

![Image p214](../../../assets/images/ce-express/user-guide-v73/p214-img1.png)
poorest performance.
3.1.37.1 Link prediction results
After calculations, you will be able to view Profile, Interference, Performance and Capacity calculation
results.

| Parameter | Description |
|---|---|
| Carrier | Select different carriers to view the results for each one of them. |
| Diversity improvement | To alleviate the effect of multipath fading, various propagation diversity techniques are employed. |
| Protection improvement | The protection improvement factor is a ratio between unprotected and protected unavailability. Profile - The Link Profile behaves in virtually the same way as a regular profile. |

![Image p215](../../../assets/images/ce-express/user-guide-v73/p215-img1.png)

Power Budget - the calculation of the balance between transmitted power, power losses in the system,
and receiver sensitivity in a communication system.
Path Loss - the reduction in signal strength as it travels from the transmitter to the receiver.
Interference - the undesired impact of one signal on another, leading to potential signal degradation.
Performance - assessments of key metrics like data rate, error rates, and signal-to-noise ratio, crucial for

![Image p216](../../../assets/images/ce-express/user-guide-v73/p216-img1.png)

![Image p216](../../../assets/images/ce-express/user-guide-v73/p216-img2.png)
evaluating and optimizing a communication system's efficiency.

3.1.37.2 Interfering links
In this tab, you will be able to view interference Power Budget, Path Loss, Profile, and Spectrum Mask

![Image p217](../../../assets/images/ce-express/user-guide-v73/p217-img1.png)

![Image p217](../../../assets/images/ce-express/user-guide-v73/p217-img2.png)

![Image p217](../../../assets/images/ce-express/user-guide-v73/p217-img3.png)
results in an unordered fashion.
Profile - The Link Profile behaves in virtually the same way as a regular profile.
Power Budget - the calculation of the balance between transmitted power, power losses in the system,

and receiver sensitivity in a communication system.
Path Loss - the reduction in signal strength as it travels from the transmitter to the receiver.
Spectrum Mask - the method used to assess the usage efficiency of a frequency spectrum in a
telecommunications system, involving the measurement of how much and how effectively different
frequencies are being utilized.
3.1.37.3 Generate report
The calculation results can be automatically transferred into a Link Prediction Report. This report will
show profile, prediction parameter and results, performance and propagation reliability. The report can be

![Image p218](../../../assets/images/ce-express/user-guide-v73/p218-img1.png)

![Image p218](../../../assets/images/ce-express/user-guide-v73/p218-img2.png)
exported in PDF format.

Report example:

![Image p219](../../../assets/images/ce-express/user-guide-v73/p219-img1.png)

![Image p219](../../../assets/images/ce-express/user-guide-v73/p219-img2.png)
