# 4. Cell Prediction

## Cell structure

- Physical parameters

- Coordinates

- Height

- Azimuth

- …

- Logical parameters

- Power

- Bandwidth

- Frequency

- …

![Slide 2](../../../assets/images/ce-pro/training-pdf-04-cell-prediction/page-2.png)

## Cell: Coordinates

- Projected coordinate system:

- X

- Y

- Geographic coordinate system in meters:

- Longitude

- Latitude

- Z – total cell height above sea level.

![Slide 3](../../../assets/images/ce-pro/training-pdf-04-cell-prediction/page-3.png)

## Cell Name

- Unique parameter in the project.

- Best server – the same.

![Slide 4](../../../assets/images/ce-pro/training-pdf-04-cell-prediction/page-4.png)

## General cells parameter

Value          CE Field        Units        Example                                             Description Latitude              latitude             Meters   49.9993        Y point coordinate in Decimal degrees and in WGS 1984 geographical coordinate system.

Longitude             longitude            Meters   33.6573        X point coordinate in Decimal degrees and in WGS 1984 geographical coordinate system.

Cell identification   cell_name            [text]   5G cell XXYY   Represents cell identification, usually name. Site identification   site_name            [text]   Site 55 ID     Represents site identification, usually name. Cell height           height               meters   40             Cell height above the ground. Cell azimuth          azimuth              degree   50             Cell direction from the north, value ranges from 0 to 360. Mechanical tilt       tilt                 degree   1              Cell mechanical tilt value. Frequency             frequency            MHz      3500           Frequency value in MHz. Power                 power                dBm      40             Based on Workspace parameter, it can be only Cell power, and EIRP will be calculated from antenna gain and misc loss. It can represent EIRP value too, if Workspace parameter Calculate EIRP is defined to No. Antenna Gain          Antenna_gain         dBi      18.2           Gain of antenna which is assigned for Cell. Misc. Loss            Misc_loss            dB       1              Total Cell loss. Bandwidth             bandwidth            MHz      0.015          Cell bandwidth value in MHz. Especially required for 3G, 4G, and 5G technologies.

Subcarrier spacing    Subcarrier_spacing   kHz      15             Especially required for 5G, as 4G uses constant value 15. MIMO configuration    tx_mimo              Number 4                Transmitter MIMO configuration, possible values 1, 2, 4, 8, 16, 32, 64. MIMO configuration    rx_mimo              Number 4                Receiver MIMO configuration, possible values 1, 2, 4, 8, 16, 32, 64. Cell load             cell_load            Percent 30              Parameter ranges are from 0 to 100 percent. Describes how the cell is loaded in real-time. Load is taken for broadband calculations.

Technology            technology           Text     2G             Possible values: 2G, 3G, 4G, 5G. Describes cell technology.

Antenna name          antenna_id           Number 1                Represents Antenna ID value.

![Slide 5](../../../assets/images/ce-pro/training-pdf-04-cell-prediction/page-5.png)

## RF Predictions structure

- Predictions

- Results

- Temp

![Slide 6](../../../assets/images/ce-pro/training-pdf-04-cell-prediction/page-6.png)

## Exercise

Description: C:\CE_Course\0. Descriptions

Name: 4. Cell Prediction.pdf

![Slide 7](../../../assets/images/ce-pro/training-pdf-04-cell-prediction/page-7.png)
