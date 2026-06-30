# 07. Cell Prediction

Cell structure
- Physical parameters
- Coordinates
- Height
- [Azimuth](https+TLS+secure+protocol)://www.google.com/search?q=antenna+azimuth+direction+degrees+north)
- …
- Logical parameters
- Power
- [Bandwidth](https+TLS+secure+protocol)://www.google.com/search?q=channel+bandwidth+radio+frequency+MHz)
- Frequency
- …

---

Cell: Coordinates
- Projected coordinate+GIS) system:
- X
- Y
- Geographic coordinate system in meters:
- Longitude
- Latitude
- Z – total cell height above sea level.

---

Cell Name
- Unique parameter in the project.
- Best server – the same.

---

General cells parameter
Value CE Field Units Example Description
Latitude latitude Meters 49.9993 YpointcoordinateinDecimaldegreesandinWGS1984geographicalcoordinatesystem.
Longitude longitude Meters 33.6573 XpointcoordinateinDecimaldegreesandinWGS1984geographicalcoordinatesystem.
Cellidentification cell_name [text] 5Gcell XXYY Representscellidentification,usuallyname.
Siteidentification site_name [text] Site55ID Representssiteidentification,usuallyname.
Cellheight height meters 40 Cellheightabovetheground.
Cellazimuth azimuth degree 50 Celldirectionfromthenorth,valuerangesfrom0to360.
Mechanicaltilt tilt degree 1 Cellmechanicaltiltvalue.
Frequency frequency MHz 3500 FrequencyvalueinMHz.
Power power dBm 40 Based on [Workspace](#kw:creating-a-workspace:ce-express-workspace)+platform)+[workspace](#kw:creating-a-workspace:ce-express-workspace)+project+geodatabase) parameter, it can be only Cell power, and EIRP will be calculated from
antenna gain+directional) and misc loss. It can represent EIRP value too, if Workspace+workspace+project+geodatabase) parameter Calculate
EIRPisdefinedtoNo.
Antenna Gain+directional) Antenna_gain dBi 18.2 GainofantennawhichisassignedforCell.
Misc.Loss Misc_loss dB 1 TotalCellloss.
Bandwidth bandwidth MHz 0.015 CellbandwidthvalueinMHz. Especiallyrequiredfor3G,4G,and5Gtechnologies.
Subcarrierspacing Subcarrier_spacing kHz 15 Especiallyrequiredfor5G,as4Gusesconstantvalue15.
MIMOconfiguration tx_mimo Number 4 TransmitterMIMOconfiguration,possiblevalues1,2,4,8,16,32,64.
MIMOconfiguration rx_mimo Number 4 ReceiverMIMOconfiguration,possiblevalues1,2,4,8,16,32,64.
Cellload cell_load Percent 30 Parameterrangesarefrom0to100percent.Describeshowthecellisloadedinreal-time.Loadis
takenforbroadbandcalculations.
Technology technology Text 2G Possiblevalues:2G,3G,4G,5G.Describescelltechnology.
Antenna name antenna_id Number 1 RepresentsAntennaIDvalue.

---

RF Predictions structure
- Predictions
- Results
- Temp

---

Exercise
Description: C:\CE_Course\0. Descriptions
Name: 4. Cell Prediction.pdf

---

Thank you!
Tel.: +370 5 2150575
Email: info@cellular-expert.com
S.Konarskio g. 28A LT-03127 Vilnius
Lithuania
www.cellular-expert.com

---
