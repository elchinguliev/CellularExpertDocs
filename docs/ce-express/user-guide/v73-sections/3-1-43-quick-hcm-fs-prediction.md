# 3.1.43 Quick HCM-FS prediction

Click this button to open Quick HCM-FS prediction tool.
This performs calculations between two HCM-FS files.
Calculation name
Name of the calculation.

Trigger options are used to limit the size of calculation report. If all trigger options are disabled, calculation

![Image p237](../../../assets/images/ce-express/user-guide-v73/p237-img1.png)

![Image p237](../../../assets/images/ce-express/user-guide-v73/p237-img2.png)

![Image p237](../../../assets/images/ce-express/user-guide-v73/p237-img3.png)
report may become very huge since all calculation cases will be logged into the report.
Limit TD
If enabled, calculation case is logged into the report only if threshold degradation is greater than defined.
TD, dB >
Value of threshold degradation used as a trigger for logging calculation case into the report.
Limit Interference
If enabled, calculation case is logged into the report only if interference level is greater than defined. Can
be used along with TD limit.
Interference level, dBW
Value of interference level used as a trigger for logging calculation case into the report.
Distance PTX to RX [km]
Distance between passive transmitter and receiver. In the case of passive receiver, calculation will be
performed only if distance between passive transmitter and receiver is less than defined. Decision
whether include this calculation into the report will additionally depend on the rest of Trigger options.
Please note that all calculation cases resulted in errors will be logged into the report regardless of Trigger
options.
Reference file
File against which test calculations are performed.
Test file

File that is tested against reference file.
There is no substantial difference between test and reference file. Calculations will be performed in the
same way but the calculation report always lists records of test file.
When calculation report is opened it shows all the records from test file along with maximum value of
threshold degradation.
| Parameter | Description |
|---|---|
| Type | Type of station of the test record |
| Name | Name os station of the test record |
| Frequency | Combines frequency and frequency unit of the test record |
| Reference | Coordination reference of the test record |
| Original status | Status of coordination of the test record |
Max TD
Maximum threshold degradation. In case of test TX record, it shows maximum threshold degradation
caused by the transmitter to a receiver of the reference file. In case of test RX record, it shows threshold

![Image p238](../../../assets/images/ce-express/user-guide-v73/p238-img1.png)
degradation of this particular receiver. For PTX or PRX test record, it shows maximum threshold
degradation of either test or reference receiver.

Show interference list - shows list of calculated stations against particular test record.
Clicking on Profile button allows user to perform detailed HCM calculations.
