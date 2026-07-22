# 3.1.6 Antennas

Click this button ![icon](../../../assets/images/ce-express/user-guide-v73/p075-img2.png) to open Antennas tool.
Preview the list of available antennas in the project. The antennas are used for point-to-area calculations.

![Image p75](../../../assets/images/ce-express/user-guide-v73/p075-img1.png)

Search
Initiates the search procedure in the antennas list.
Delete antenna
Delete antenna using Delete button.
Click on an antenna to preview the [antenna patterns](#kw:importing-antenna-patterns:ce-express-antenna).

![Image p76](../../../assets/images/ce-express/user-guide-v73/p076-img1.png)

![Image p76](../../../assets/images/ce-express/user-guide-v73/p076-img2.png)

Adjust vertical pattern
In the case where you have an electrically tilted vertical [antenna pattern](#kw:managing-the-antenna-library:ce-express-antenna) imported, you might want to tilt it
back so it is essentially a 0 tilt [antenna pattern](#kw:managing-the-antenna-library:ce-express-antenna) (recommended if you use electrical tilt field in cell attributes).
You may use the adjust vertical pattern tool to do this. Find the center of the main lobe of the vertical
[antenna pattern](#kw:managing-the-antenna-library:ce-express-antenna) using the “main lobe center” slider, then click accept.

![Image p77](../../../assets/images/ce-express/user-guide-v73/p077-img1.png)

![Image p77](../../../assets/images/ce-express/user-guide-v73/p077-img2.png)

3.1.6.1 Import Antennas
To import new antennas, click the New Antenna button
and then select Import Files.
To start the import procedure, select or drag and drop the antenna pattern file. Planet format antenna

![Image p78](../../../assets/images/ce-express/user-guide-v73/p078-img1.png)

![Image p78](../../../assets/images/ce-express/user-guide-v73/p078-img2.png)

![Image p78](../../../assets/images/ce-express/user-guide-v73/p078-img3.png)

![Image p78](../../../assets/images/ce-express/user-guide-v73/p078-img4.png)
pattern files are supported. Here is an example:

3.1.6.1 Import HCM code file
To import HCM code patterns as antennas, you may use this import option. The required file is a CSV with
3 fields, antenna gain, horizontal HCM code and vertical HCM code. These are then combined and imported
as antenna patterns under the HCM manufacturer group. Multiple lines are allowed.
CSV file example:
After file upload, you are prompted to assign which CSV field corresponds to the required parameters:
3.1.6.2 Import cell array antenna
If you have separate pattern files for a multibeam antenna, you may use this import option to combine them

![Image p79](../../../assets/images/ce-express/user-guide-v73/p079-img1.png)

![Image p79](../../../assets/images/ce-express/user-guide-v73/p079-img2.png)
into a single cell array antenna pattern.

Antenna parameters
| Parameter | Description |
|---|---|
| Manufacturer | Antenna manufacturer. |
| Model | Antenna name. |
| Frequency | Antenna frequency value in MHz. |
| Gain | Antenna gain value in dBi. |

![Image p80](../../../assets/images/ce-express/user-guide-v73/p080-img1.png)

3.1.6.3 Create manually
To manually create an antenna, click the New Antenna button
and then select Create Manually.

![Image p81](../../../assets/images/ce-express/user-guide-v73/p081-img1.png)

![Image p81](../../../assets/images/ce-express/user-guide-v73/p081-img2.png)

![Image p81](../../../assets/images/ce-express/user-guide-v73/p081-img3.png)

Antenna parameters
Manufacturer
Antenna manufacturer (company or entity).
Model
Antenna name.

![Image p82](../../../assets/images/ce-express/user-guide-v73/p082-img1.png)

| Parameter | Description |
|---|---|
| Frequency | Antenna frequency value in MHz. |
| Gain | Antenna gain value in dBi. |
| Max attenuation | Attenuation value assigned to the attenuated parts of the antenna pattern |
Horizontal pattern
| Parameter | Description |
|---|---|
| Beamwidth | Antenna’s vertical beamwidth value in degrees. Used for generating the antenna pattern. |
| Smoothing degree count | Transition width between attenuated and non-attenuated parts of the antenna pattern in degrees. The attenuation values are linearly interpolated between 0 and the max attenuation value within this transition range. |
| Angle offset | Transition width between attenuated and non-attenuated parts of the antenna pattern in degrees. The attenuation values are linearly interpolated between 0 and the max attenuation value within this transition range. |
| Mirror pattern | Ability to mirror the vertical attenuation pattern. |
Pattern preview
