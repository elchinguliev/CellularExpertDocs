# 3.1.6 Antennas

Click this button ![icon](../../../assets/images/ce-express/user-guide-v73/p075-img2.png) to open Antennas tool.

Preview the list of available antennas in the project. The antennas are used for point-to-area calculations.

![Image p076](../../../assets/images/ce-express/user-guide-v73/p076-img1.png)

**Search**
Initiates the search procedure in the antennas list.

**Delete antenna**
Delete antenna using *Delete* button.

![Image p076](../../../assets/images/ce-express/user-guide-v73/p076-img2.png)

Click on an antenna to preview the [antenna patterns](#kw:importing-antenna-patterns:ce-express-antenna).

![Image p077](../../../assets/images/ce-express/user-guide-v73/p077-img1.png)

**Adjust vertical pattern**
In the case where you have an electrically tilted vertical [antenna pattern](#kw:managing-the-antenna-library:ce-express-antenna) imported, you might want to tilt it
back so it is essentially a 0 tilt [antenna pattern](#kw:managing-the-antenna-library:ce-express-antenna) (recommended if you use electrical tilt field in cell attributes).
You may use the adjust vertical pattern tool to do this. Find the center of the main lobe of the vertical
[antenna pattern](#kw:managing-the-antenna-library:ce-express-antenna) using the "main lobe center" slider, then click accept.

![Image p077](../../../assets/images/ce-express/user-guide-v73/p077-img2.png)

## 3.1.6.1 Import Antennas

To import new antennas, click the *New Antenna* button

![Image p078](../../../assets/images/ce-express/user-guide-v73/p078-img1.png)

and then select *Import Files*.

![Image p078](../../../assets/images/ce-express/user-guide-v73/p078-img2.png)

![Image p078](../../../assets/images/ce-express/user-guide-v73/p078-img3.png)

To start the import procedure, select or drag and drop the antenna pattern file. Planet format antenna
pattern files are supported. Here is an example:

![Image p078](../../../assets/images/ce-express/user-guide-v73/p078-img4.png)

## 3.1.6.2 Import HCM code file
To import HCM code patterns as antennas, you may use this import option. The required file is a CSV with
3 fields, antenna gain, horizontal HCM code and vertical HCM code. These are then combined and imported
as antenna patterns under the HCM manufacturer group. Multiple lines are allowed.

CSV file example:

![Image p079](../../../assets/images/ce-express/user-guide-v73/p079-img1.png)

After file upload, you are prompted to assign which CSV field corresponds to the required parameters:

![Image p079](../../../assets/images/ce-express/user-guide-v73/p079-img2.png)

## 3.1.6.3 Import cell array antenna

If you have separate pattern files for a multibeam antenna, you may use this import option to combine them
into a single cell array antenna pattern.

![Image p080](../../../assets/images/ce-express/user-guide-v73/p080-img1.png)

**Antenna parameters**

**Manufacturer**
Antenna manufacturer.

**Model**
Antenna name.

**Frequency**
Antenna frequency value in MHz.

**Gain**
Antenna gain value in dBi.

![Image p081](../../../assets/images/ce-express/user-guide-v73/p081-img1.png)

## 3.1.6.4 Create manually

To manually create an antenna, click the *New Antenna* button

![Image p081](../../../assets/images/ce-express/user-guide-v73/p081-img2.png)

and then select *Create Manually*.

![Image p081](../../../assets/images/ce-express/user-guide-v73/p081-img3.png)

**Antenna parameters**

**Manufacturer**
Antenna manufacturer (company or entity).

**Model**
Antenna name.

![Image p082](../../../assets/images/ce-express/user-guide-v73/p082-img1.png)

**Frequency**
Antenna frequency value in MHz.

**Gain**
Antenna gain value in dBi.

**Max attenuation**
Attenuation value assigned to the attenuated parts of the antenna pattern.

**Horizontal pattern**

**Beamwidth**
Antenna's vertical beamwidth value in degrees. Used for generating the antenna pattern.

**Smoothing degree count**
Transition width between attenuated and non-attenuated parts of the antenna pattern in degrees. The attenuation values are linearly interpolated between 0 and the max attenuation value within this transition range.

**Angle offset**
Transition width between attenuated and non-attenuated parts of the antenna pattern in degrees. The attenuation values are linearly interpolated between 0 and the max attenuation value within this transition range.

**Mirror pattern**
Ability to mirror the vertical attenuation pattern.

**Pattern preview**
