# 09. Importing Data

Network [import]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=data+import+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) for CE for [ArcGIS Pro](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+Pro+Esri+desktop+software)
- From:
- Excel
- [CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)
- [SDE](https://www.google.com/search?q=SDE+ArcSDE+spatial+database+engine) table
- To Cellular Expert [Workspace]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+workspace+project+geodatabase):
- gdb database

---

[Network objects](https://www.google.com/search?q=radio+network+objects+sites+cells+GIS)
- Cells
- Sites
- Sites (if siteid
parameter is
defined)

---

Mapping file
- [Json](https://www.google.com/search?q=JSON+JavaScript+Object+Notation+data+format) type file, can be edited with Notepad

---

Mapping file structure
- “current_name” - name of the value that is written in the data file.
As an example “freq_mhz” is a column name in the data file and will
be changed to “frequency” when the mapping file is applied and
objects are imported.
- “destination_name” - the proper name of the property (table
column name) in the Cellular
- “default_value” – The default value applies when an object in the
data file lacks a specific property. The same value will be applied for
all imported objects.

---

Cells: generate [Cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) Name
- Check option: Generate [Cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) Name
- Latitude
- Longitude
- [Azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north)
- Frequency
- Power
- Height
- [Antenna gain](https://www.google.com/search?q=antenna+gain+[dBi](https://www.google.com/search?q=dBi+decibel+isotropic+antenna+gain)+directional)

---

Apply prediction model
- Polygon type [feature class](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+feature+class+[geodatabase](https://www.google.com/search?q=ArcGIS+geodatabase+spatial+database))/shape file
- ModelID and ConfigID is a must
- Option appears when [Import](https://www.google.com/search?q=data+import+GIS+network+objects+CSV) HCM patterns option is active.

---

Parameters for Cell object
cell_name – cell identifier (recommended unique value).
latitude - Decimal degrees Y type coordinate in the WGS 1984 geographical
[coordinate system](https://www.google.com/search?q=coordinate+reference+system+CRS+GIS).
longitude - Decimal degrees X type coordinate in the WGS 1984 geographical
[coordinate system](https://www.google.com/search?q=coordinate+reference+system+CRS+GIS).
height – Cell height above the [terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography).
[azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north) - Cell direction from the North in degrees.
tilt - [Mechanical tilt](https://www.google.com/search?q=mechanical+tilt+antenna+[downtilt](https://www.google.com/search?q=antenna+downtilt+mechanical+electrical+degrees)) value.
frequency - Frequency value in [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit).
power - Power value in [dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit).
antenna_gain - [Antenna gain](https://www.google.com/search?q=antenna+gain+[dBi](https://www.google.com/search?q=dBi+decibel+isotropic+antenna+gain)+directional) value from the applied antenna.
misc_loss - Miscellaneous loss value in [dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit).

---

Parameters for Cell object
[bandwidth](https://www.google.com/search?q=channel+bandwidth+radio+frequency+[MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit)) - Value in MHz. Required for [4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology) and [5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network) technologies. For other technologies
define the value as 0.015.
noise_figure - Value in [dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit). Required for [4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology) and [5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network) technologies.
downlink_duplex_factor - Value range from 0 to 1. Required for 4G and 5G technologies, and
used for Downlink [Throughput](https://www.google.com/search?q=network+throughput+downlink+uplink+[capacity](https://www.google.com/search?q=network+capacity+planning+telecom)) calculations.
subcarrier_spacing - Value in [kHz](https://www.google.com/search?q=kHz+kilohertz+frequency+unit). Required for 4G and 5G technologies. For other
technologies define value 15.
tx_mimo - Transmitter antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64.
rx_mimo - Receiver antenna count. Available values: 1, 2, 4, 8, 16, 32 and 64.
active_antenna_effect - The parameter is dedicated to smart antenna modelling. The default
value is 0, but if massive [MIMO](https://www.google.com/search?q=MIMO+Multiple+Input+Output+antenna) is used, a smart antenna effect can be included to lower the
[interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent) and boost [throughput](https://www.google.com/search?q=network+throughput+downlink+uplink+[capacity](https://www.google.com/search?q=network+capacity+planning+telecom)). Recommended
values:
For [MIMO](https://www.google.com/search?q=MIMO+Multiple+Input+Multiple+Output+antenna+technology) 32x32 – value 6.
For [MIMO](https://www.google.com/search?q=MIMO+Multiple+Input+Multiple+Output+antenna+technology) 64x64 – value 9.

---

Parameters for Cell object
cell_load - The parameter is described in percentages and varies from 0 to 100. It describes how the cell is loaded.
The Cell load affects RSSI, [RSRQ](https://www.google.com/search?q=RSRQ+Reference+Signal+Received+Quality+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+4G)), DL Throughput calculations. For example, if the Cell load is higher, the DL
Throughput is lower.
technology - Describes the technology of cell. Possible values are [2G](https://www.google.com/search?q=2G+GSM+mobile+network+second+generation), [3G](https://www.google.com/search?q=3G+UMTS+HSPA+mobile+network), 4G, 5G and WiFi.
prediction_model_id – prediction model identification:
If value 1 – [ITU-R](https://www.google.com/search?q=ITU+R+radio+communication+standard) P.452
If value 2 – UniMacro
If value 3 – CEC [ITU-R](https://www.google.com/search?q=ITU+R+International+Telecommunication+Union+Radio)
If value 4 – [LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation) [ITU-R](https://www.google.com/search?q=ITU+R+International+Telecommunication+Union+Radio) P.525
If value 5 – ITU-R P.368
prediction_model_configuration_id – prediction model configuration identification in define prediction model
(prediction_model_id value).
frequency_group – helps to manage different frequency groups, [RF prediction](https://www.google.com/search?q=RF+radio+frequency+prediction+coverage) will do separate prediction for
different frequency_group value automatically.
antenna_id- antenna identification in the database.
duplex_mode - Required for 4G and 5G technologies, possible values [FDD](https://www.google.com/search?q=FDD+Frequency+Division+Duplex+LTE) or [TDD](https://www.google.com/search?q=TDD+Time+Division+Duplex+LTE+5G).
site_id – to automatically create [Site](https://www.google.com/search?q=cell+site+tower+base+station+location) object for cells, define [site](https://www.google.com/search?q=cell+site+tower+base+station+location) name field here. Must be a text format.

---

Exercise
Description: C:\CE_Course\0. Descriptions
Name: 6. Importing data.pdf

---

Thank you!
Tel.: +370 5 2150575
Email: info@cellular-expert.com
S.Konarskio g. 28A LT-03127 Vilnius
Lithuania
www.cellular-expert.com

---
