# 3.1.39 Link HCM-FS prediction

Click this button ![icon](../../../assets/images/ce-express/user-guide-v73/p222-img2.png) to open Link HCM-FS prediction tool.
This calculates interference between selected links and HCM-FS records available in the database.
Calculation settings

![Image p222](../../../assets/images/ce-express/user-guide-v73/p222-img1.png)

![Image p222](../../../assets/images/ce-express/user-guide-v73/p222-img3.png)

Calculation name
Name of the calculation.
Link template
Template to be used for filling up missing parameters of the link.
Trigger options
Trigger options are used to limit the size of calculation report. If all trigger options are disabled, calculation

![Image p223](../../../assets/images/ce-express/user-guide-v73/p223-img1.png)
report may become very huge since all calculation cases will be logged into the report.
| Parameter | Description |
|---|---|
| Limit TD | If enabled, calculation case is logged into the report only if threshold degradation is greater than defined. |
| TD, dB > | Value of threshold degradation used as a trigger for logging calculation case into the report. |
| Limit Interference | If enabled, calculation case is logged into the report only if interference level is greater than defined. Can be used along with TD limit. |
| Interference level, dBW | Value of interference level used as a trigger for logging calculation case into the report. |
Distance PTX to RX [km]
Distance between passive transmitter and receiver. In the case of passive receiver, calculation will be
performed only if distance between passive transmitter and receiver is less than defined. Decision
whether to include this calculation into the report will additionally depend on the rest of Trigger options.
3.1.39.1 Link HCM-FS prediction results

Report lists all the selected links and following parameters:
- Maximum outgoing TD, dB. Maximum interference (threshold degradation) to a single HCM-FS
receiver caused by the link.
- Maximum incoming TD, dB. Maximum interference (threshold degradation) from HCM-FS
transmitter to the receiver of the link.
Show incoming interference.
Displays list of HCM-FS transmitters calculated against receivers of the link.
List shows site of the affected link, HCM-FS parameters and interference calculation result.

![Image p224](../../../assets/images/ce-express/user-guide-v73/p224-img1.png)

![Image p224](../../../assets/images/ce-express/user-guide-v73/p224-img2.png)

![Image p224](../../../assets/images/ce-express/user-guide-v73/p224-img3.png)
