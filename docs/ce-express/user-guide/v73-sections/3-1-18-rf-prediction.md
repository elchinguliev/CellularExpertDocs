# 3.1.18 RF Prediction

Click this button ![icon](../../../assets/images/ce-express/user-guide-v73/p153-img2.png) to open RF Prediction tool.
This tool allows to perform predictions for cell objects selected on the map. Calculations can be performed

![Image p153](../../../assets/images/ce-express/user-guide-v73/p153-img1.png)

![Image p153](../../../assets/images/ce-express/user-guide-v73/p153-img3.png)
for more than one cell at the same time. Use the Features tool to select cells on the map.

The selected cell count is visible in the RF Prediction dialog.
The cells are split into technologies automatically. The cell’s technology is defined by the attributes in the

![Image p154](../../../assets/images/ce-express/user-guide-v73/p154-img1.png)

![Image p154](../../../assets/images/ce-express/user-guide-v73/p154-img2.png)

![Image p154](../../../assets/images/ce-express/user-guide-v73/p154-img3.png)
technology field.
To preview the calculation parameters, use the expand option for the technology.

Select the technology with the switch button and press Calculate to initiate the predictions. The prediction

![Image p155](../../../assets/images/ce-express/user-guide-v73/p155-img1.png)
will be added to the Prediction History dialog.

3.1.18.1 2G technology (GSM/CDMA-850/TETRA/P-25)

![Image p156](../../../assets/images/ce-express/user-guide-v73/p156-img1.png)

Resolution
Prediction raster cell size in meters.
Best server count
There is the possibility to calculate up to 5 best servers. The prediction rasters show the 1st, 2nd, 3rd, and so
on strongest signal sources.
Cell template
If the cell is missing the required parameters, the parameters from the template will be used.
Repeater template
If the repeater is missing the required parameters, the parameters from the template will be used.
Calculate interference
The interference for 2G cells will be calculated. Note that for this calculation the C/I and C/A thresholds
must be defined.
C/I Max Field Margin, dB
The corresponding channel’s signal interference if the first and the second strongest signals differ by less
than or equal to 10 dBm.
C/A Max Field Margin, dB

The neighboring channel’s signal interference if the first and the second strongest signals differ by less than
or equal to 10 dBm.
| Parameter | Description |
|---|---|
| Calculate uplink | An option to calculate the Uplink signal strength. |
| RX EIRP, dBm | The power that the receiving antenna can capture from the transmitted signal in dBm. |
| Calculate technology totals | Calculates the overall field strength and the aggregate downlink throughput for several frequency bands in the same technology. |
| Calculate neighbours | An option to calculate neighbours for each cell in the technology section |
Minimum FS
Field strength threshold in dBm above which the area is considered as “covered” by the cell. The same
threshold is used for calculating whether a cell’s potential neighboring cell has overlapping areas, I.e. cells
only overlap where both of their coverage field strength values are above this threshold.
Neighbour minimum coverage
Coverage area overlap percentage above which a cell is considered a neighbour.
Maximum neighbour count
Maximum number of neighbours a cell can have. If a cell has more potential neighbours than this number,
only the ones with the highest overlap are returned.
Available coverage rasters:
- Received signal level raster in dBm, within the channel bandwidth appropriate to this technology.
It is possible to calculate separately the rasters for the 1st, 2nd, 3rd, 4th and 5th strongest signal levels,
and it depends on the count defined in the Best server count option.
- The best server raster shows the identification of cells generating the strongest signals at each
pixel. Raster count depends on the Best server count parameter value specified by the user.
o 1st best server shows the serving cell with the strongest field strength.
o 2nd best server shows the second strongest field strength cell identification.
o 3rd best server shows third shows the strongest field strength cell identification.
o 4th best server fourth shows the strongest field strength cell identification.
o 5th best server shows the fifth shows the strongest field strength cell identification.
- C/I rasters show Carrier-to-interference ratio in dB, to account for inter-cell interference from nearby
cells that utilise the same carrier.
- C/A raster show Carrier-to-Adjacent interference ratio in dB, to account for inter-cell interference
from nearby cells that operate the adjacent carrier (adjacent frequency channel).
- Uplink Field Strength raster shows receiver signal strength in dBm.

3.1.18.2 3G technology (UMTS/CDMA)

![Image p158](../../../assets/images/ce-express/user-guide-v73/p158-img1.png)

| Parameter | Description |
|---|---|
| Resolution | Prediction raster cell size in meters. |
| Best server count | 1st, 2nd, 3rd, There is the possibility to calculate up to 5 best servers. The prediction rasters show the and so on strongest signal sources. |
| Cell template | If the cell is missing the required parameters, the parameters from the template will be used. |
| Repeater template | If the repeater is missing the required parameters, the parameters from the template will be used. |
Calculate FS overlap

This calculation in Cellular Expert calculates the geographical areas where two different cells provide similar
signal strength. Specifically, it identifies regions where the absolute difference between the field strengths
of Cell 1 and Cell 2 is less than a defined threshold (e.g., 10 dB). This analysis is useful for understanding
coverage overlaps and potential handover zones between cells.
| Parameter | Description |
|---|---|
| FS overlap minimum FS | Defines the lowest acceptable field strength for overlap consideration. |
| FS overlap max field margin | Threshold under which the cell field strength overlap values are presented in the results. |
| Calculate uplink | An option to calculate the Uplink signal strength. |
| RX EIRP, dBm | The power that the receiving antenna can capture from the transmitted signal in dBm. Calculate technology totals |
| Calculate technology totals | Calculates the overall field strength and the aggregate downlink throughput for several frequency bands in the same technology. |
| Calculate neighbours | An option to calculate neighbours for each cell in the technology section |
Minimum FS
Field strength threshold in dBm above which the area is considered as “covered” by the cell. The same
threshold is used for calculating whether a cell’s potential neighboring cell has overlapping areas, I.e. cells
only overlap where both of their coverage field strength values are above this threshold.
Neighbour minimum coverage
Coverage area overlap percentage above which a cell is considered a neighbour.
Maximum neighbour count
Maximum number of neighbours a cell can have. If a cell has more potential neighbours than this number,
only the ones with the highest overlap are returned.
Available coverage rasters:
- Received signal level raster in dBm, within the channel bandwidth appropriate to this technology.
It is possible to calculate separately the rasters for 1st, 2nd, 3rd, 4th and 5th strongest signal level
rasters, and it depends on the count defined in Best server count option.
- The best server raster shows the identification of cells generating the strongest signals at each
pixel. Raster count depends on the Best server count parameter value specified by the user.
o 1st best server shows the serving cell with the strongest field strength.
o 2nd best server shows the second strongest field strength cell identification.
o 3rd best server shows third shows the strongest field strength cell identification.
o 4th best server fourth show the strongest field strength cell identification.
o 5th best server shows the fifth shows the strongest field strength cell identification.
- Uplink Field Strength raster shows receiver signal strength in dBm.

3.1.18.3 4G technology (LTE/BWA/WiMAX)

![Image p160](../../../assets/images/ce-express/user-guide-v73/p160-img1.png)

Resolution
Prediction raster cell size in meters.
Best server count
There is the possibility to calculate up to 5 best servers. The prediction rasters show the 1st, 2nd, 3rd, and so
on strongest signal sources. We recommend to use at least 3 best servers for more precise RSRQ, RSSI,
SINR, and Throughput calculations.

Cell template
If the cell is missing the required parameters, the parameters from the template will be used.
Repeater template
If the repeater is missing the required parameters, the parameters from the template will be used.
Calculate FS overlap
This calculation in Cellular Expert calculates the geographical areas where two different cells provide similar
signal strength. Specifically, it identifies regions where the absolute difference between the field strengths
of Cell 1 and Cell 2 is less than a defined threshold (e.g., 10 dB). This analysis is useful for understanding
coverage overlaps and potential handover zones between cells.
| Parameter | Description |
|---|---|
| FS overlap minimum FS | Defines the lowest acceptable field strength for overlap consideration. |
| FS overlap max field margin | Threshold under which the cell field strength overlap values are presented in the results. |
| Calculate uplink | An option to calculate the Uplink signal strength. |
| Rx EIRP, dBm | The EIRP value of the receiver in dBm. |
| BS RX Noise Floor, dB | Best Server receiver’s lowest noise level. No values below this level will be included in the calculation. |
| UL interference ceiling, dB | Uplink’s interference highest value. No values above this point will be included in the calculation. |
| Calculate broadband coverage | An option to calculate the Broadband coverage. • RSSI; • RSRQ; RS-SINR; • DL Throughput. • |
| Calculate technology totals | Calculates the overall field strength and the aggregate downlink throughput for several frequency bands in the same technology. |
| Calculate neighbours | An option to calculate neighbours for each cell in the technology section |
Minimum FS
Field strength threshold in dBm above which the area is considered as “covered” by the cell. The same
threshold is used for calculating whether a cell’s potential neighboring cell has overlapping areas, I.e. cells
only overlap where both of their coverage field strength values are above this threshold.
Neighbour minimum coverage
Coverage area overlap percentage above which a cell is considered a neighbour.

Maximum neighbour count
Maximum number of neighbours a cell can have. If a cell has more potential neighbours than this number,
only the ones with the highest overlap are returned.
Available coverage rasters:
- Reference Signal Receive Power ([RSRP](#kw:typical-rsrp-thresholds:ce-express-rf-prediction)) raster in dBm, as measured for a reference OFDMA sub-
carrier bandwidth. It is possible to calculate separately the rasters for the 1st, 2nd, 3rd, 4th and 5th
strongest signal levels and it depends on the count defined in the Best server count option.
- The best server raster shows the identification of cells that generate the strongest signals at each
pixel. Raster count depends on the Best server count parameter value specified by the user.
o 1st best server shows the serving cell with the strongest field strength.
o 2nd best server shows the second strongest field strength cell identification.
o 3rd best server shows third show strongest field strength cell identification.
o 4th best server fourth shows the strongest field strength cell identification.
o 5th best server shows the fifth shows the strongest field strength cell identification.
- Received Signal Strength Indicator (RSSI) estimated values' raster in dBm.
- Reference Signal Receive Quality (RSRQ) estimated values’ raster in dB.
- Reference Signal’s – Signal to Inteference and Noise Ratio (RS-SINR) estimated values’ raster in
dB.
- Estimated achievable Downlink Throughput values’ raster in Mbps.
- Uplink Field strength raster in dBm.
- Uplink SINR raster
- Uplink Throughput

3.1.18.4 5G technology (NR/CBRS)

![Image p163](../../../assets/images/ce-express/user-guide-v73/p163-img1.png)

Resolution
Prediction raster cell size in meters.
Best server count
There is the possibility to calculate up to 5 best servers. The prediction rasters show the 1st, 2nd, 3rd, and so
on strongest signal sources. We recommend to use at least 3 best servers for more precise RSRQ, RSSI,
SINR, and Throughput calculations.
Cell template
If the cell is missing the required parameters, the parameters from the template will be used.

Repeater template
If the repeater is missing the required parameters, the parameters from the template will be used.
Calculate FS overlap
This calculation in Cellular Expert calculates the geographical areas where two different cells provide similar
signal strength. Specifically, it identifies regions where the absolute difference between the field strengths
of Cell 1 and Cell 2 is less than a defined threshold (e.g., 10 dB). This analysis is useful for understanding
coverage overlaps and potential handover zones between cells.
| Parameter | Description |
|---|---|
| FS overlap minimum FS | Defines the lowest acceptable field strength for overlap consideration. |
| FS overlap max field margin | Threshold under which the cell field strength overlap values are presented in the results. |
| Calculate uplink | An option to calculate the Uplink signal strength. |
| Rx EIRP, dBm | The EIRP value of the receiver in dBm. |
| BS RX Noise Floor, dB | Best Server receiver’s lowest noise level. No values below this level will be included in the calculation. |
| UL interference ceiling, dB | Uplink’s interference highest value. No values above this point will be included in the calculation. |
| Calculate broadband coverage | An option to calculate the Broadband coverage. RSSI; • RSRQ; • • RS-SINR; DL Throughput. • |
| Calculate technology totals | Calculates the overall field strength and the aggregate downlink throughput for several frequency bands in the same technology. |
| Calculate neighbours | An option to calculate neighbours for each cell in the technology section |
Minimum FS
Field strength threshold in dBm above which the area is considered as “covered” by the cell. The same
threshold is used for calculating whether a cell’s potential neighboring cell has overlapping areas, I.e. cells
only overlap where both of their coverage field strength values are above this threshold.
Neighbour minimum coverage
Coverage area overlap percentage above which a cell is considered a neighbour.
Maximum neighbour count
Maximum number of neighbours a cell can have. If a cell has more potential neighbours than this number,
only the ones with the highest overlap are returned.

Available coverage rasters:
- Equivalent Reference Signal Receive Power ([RSRP](#kw:typical-rsrp-thresholds:ce-express-rf-prediction)) raster in dBm, as measured for a reference
OFDMA sub-carrier bandwidth. It is possible to calculate separately the rasters for the 1st, 2nd, 3rd,
4th and 5th strongest signal levels and it depends on the count defined in the Best server count
option.
- The best server raster shows the identification of cells that generate the strongest signals at each
pixel. Raster count depends on the Best server count parameter value specified by the user.
o 1st best server shows the serving cell with the strongest field strength.
o 2nd best server shows the second strongest field strength cell identification.
o 3rd best server shows third shows the strongest field strength cell identification.
o 4th best server fourth shows show strongest field strength cell identification.
o 5th best server shows the fifth shows the strongest field strength cell identification.
- Received Signal Strength Indicator (RSSI) estimated values' raster in dBm.
- Reference Signal Receive Quality (RSRQ) estimated values’ raster in dB.
- Reference Signal’s Signal to Inteference and Noise Ratio (RS-SINR) estimated values’ raster in
dB.
- Estimated achievable Downlink Throughput values’ raster in Mbps.
- Uplink Field strength raster in dBm.
- Uplink SINR.
- Uplink Throughput.

3.1.18.5 WiFi technology

![Image p166](../../../assets/images/ce-express/user-guide-v73/p166-img1.png)

Resolution
Prediction raster cell size in meters.
Best server count
There is the possibility to calculate up to 5 best servers. The prediction rasters show the 1st, 2nd, 3rd, and so
on strongest signal sources. We recommend to use at least 3 best servers for more precise RSRQ, RSSI,
SINR, and Throughput calculations.

Cell template
If the cell is missing the required parameters, the parameters from the template will be used.
Repeater template
If the repeater is missing the required parameters, the parameters from the template will be used.
Calculate FS overlap
This calculation in Cellular Expert calculates the geographical areas where two different cells provide similar
signal strength. Specifically, it identifies regions where the absolute difference between the field strengths
of Cell 1 and Cell 2 is less than a defined threshold (e.g., 10 dB). This analysis is useful for understanding
coverage overlaps and potential handover zones between cells.
| Parameter | Description |
|---|---|
| FS overlap minimum FS | Defines the lowest acceptable field strength for overlap consideration. |
| FS overlap max field margin | Threshold under which the cell field strength overlap values are presented in the results. |
| Calculate uplink | An option to calculate the Uplink signal strength. |
| Rx EIRP, dBm | The EIRP value of the receiver in dBm. |
| BS RX Noise Floor, dB | Best Server receiver’s lowest noise level. No values below this level will be included in the calculation. |
| UL interference ceiling, dB | Uplink’s interference highest value. No values above this point will be included in the calculation. |
| Calculate broadband coverage | An option to calculate the Broadband coverage. • RSSI • RSRQ RS-SINR • DL Throughput • |
| Calculate technology totals | Calculates the overall field strength and the aggregate downlink throughput for several frequency bands in the same technology. |
| Calculate neighbours | An option to calculate neighbours for each cell in the technology section |
Minimum FS
Field strength threshold in dBm above which the area is considered as “covered” by the cell. The same
threshold is used for calculating whether a cell’s potential neighboring cell has overlapping areas, I.e. cells
only overlap where both of their coverage field strength values are above this threshold.
Neighbour minimum coverage
Coverage area overlap percentage above which a cell is considered a neighbour.

Maximum neighbour count
Maximum number of neighbours a cell can have. If a cell has more potential neighbours than this number,
only the ones with the highest overlap are returned.
Available coverage rasters:
- Equivalent Reference Signal Receive Power ([RSRP](#kw:typical-rsrp-thresholds:ce-express-rf-prediction)) raster in dBm, as measured for a reference
OFDMA sub-carrier bandwidth. It is possible to calculate separately the rasters for the 1st, 2nd, 3rd,
4th and 5th strongest signal levels and it depends on the count defined in the Best server count
option.
- The best server raster shows the identification of cells that generate the strongest signals at each
pixel. Raster count depends on the Best server count parameter value specified by the user.
o 1st best server shows the serving cell with the strongest field strength.
o 2nd best server shows the second strongest field strength cell identification.
o 3rd best server shows third shows the strongest field strength cell identification.
o 4th best server fourth shows show strongest field strength cell identification.
o 5th best server shows the fifth shows the strongest field strength cell identification.
- Received Signal Strength Indicator (RSSI) estimated values' raster in dBm.
- Reference Signal Receive Quality (RSRQ) estimated values’ raster in dB.
- Reference Signal’s Signal to Inteference and Noise Ratio (RS-SINR) estimated values’ raster in
dB.
- Estimated achievable Downlink Throughput values’ raster in Mbps.
- Uplink Field strength raster in dBm.
- Uplink SINR.
- Uplink Throughput.
