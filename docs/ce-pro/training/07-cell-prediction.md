# 07. Cell Prediction

[Cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) structure
- Physical parameters
- Coordinates
- Height
- [Azimuth]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=antenna+azimuth+direction+degrees+north)
- …
- Logical parameters
- Power
- [Bandwidth]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=channel+bandwidth+radio+frequency+[MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit))
- Frequency
- …

---

[Cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station): Coordinates
- [Projected coordinate](https://www.google.com/search?q=projected+coordinate+system+[UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator+projection)+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)) system:
- X
- Y
- [Geographic coordinate](https://www.google.com/search?q=geographic+coordinate+system+latitude+longitude) system in meters:
- Longitude
- Latitude
- Z – total cell height above sea level.

---

Cell Name
- Unique parameter in the project.
- [Best server](https://www.google.com/search?q=best+server+analysis+coverage+planning+RF) – the same.

---

General cells parameter
Value CE Field Units Example Description
Latitude latitude Meters 49.9993 YpointcoordinateinDecimaldegreesandinWGS1984geographicalcoordinatesystem.
Longitude longitude Meters 33.6573 XpointcoordinateinDecimaldegreesandinWGS1984geographicalcoordinatesystem.
Cellidentification cell_name [text] 5Gcell XXYY Representscellidentification,usuallyname.
Siteidentification site_name [text] Site55ID Representssiteidentification,usuallyname.
Cellheight height meters 40 Cellheightabovetheground.
Cellazimuth [azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north) degree 50 Celldirectionfromthenorth,valuerangesfrom0to360.
Mechanicaltilt tilt degree 1 Cellmechanicaltiltvalue.
Frequency frequency [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit) 3500 FrequencyvalueinMHz.
Power power [dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit) 40 Based on [Workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+workspace+project+geodatabase) parameter, it can be only Cell power, and [EIRP](https://www.google.com/search?q=EIRP+Effective+Isotropic+Radiated+Power) will be calculated from
[antenna gain](https://www.google.com/search?q=antenna+gain+[dBi](https://www.google.com/search?q=dBi+decibel+isotropic+antenna+gain)+directional) and misc loss. It can represent [EIRP](https://www.google.com/search?q=EIRP+Effective+Isotropic+Radiated+Power+antenna) value too, if [Workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase) parameter Calculate
EIRPisdefinedtoNo.
[Antenna Gain](https://www.google.com/search?q=antenna+gain+[dBi](https://www.google.com/search?q=dBi+decibel+isotropic+antenna+gain)+directional) Antenna_gain dBi 18.2 GainofantennawhichisassignedforCell.
Misc.Loss Misc_loss [dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit) 1 TotalCellloss.
[Bandwidth](https://www.google.com/search?q=channel+bandwidth+radio+frequency+MHz) bandwidth MHz 0.015 CellbandwidthvalueinMHz. Especiallyrequiredfor3G,[4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology),and5Gtechnologies.
Subcarrierspacing Subcarrier_spacing [kHz](https://www.google.com/search?q=kHz+kilohertz+frequency+unit) 15 Especiallyrequiredfor5G,as4Gusesconstantvalue15.
MIMOconfiguration tx_mimo Number 4 TransmitterMIMOconfiguration,possiblevalues1,2,4,8,16,32,64.
MIMOconfiguration rx_mimo Number 4 ReceiverMIMOconfiguration,possiblevalues1,2,4,8,16,32,64.
Cellload cell_load Percent 30 Parameterrangesarefrom0to100percent.Describeshowthecellisloadedinreal-time.Loadis
takenforbroadbandcalculations.
Technology technology Text [2G](https://www.google.com/search?q=2G+GSM+mobile+network+second+generation) Possiblevalues:[2G](https://www.google.com/search?q=2G+GSM+mobile+network+second+generation),[3G](https://www.google.com/search?q=3G+UMTS+HSPA+mobile+network),[4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology),[5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network).Describescelltechnology.
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
