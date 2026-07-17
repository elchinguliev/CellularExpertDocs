# Antennas

> **Version:** CE Express v7.3

The Antennas tool lets you preview, import, and manage antenna patterns used in point-to-area calculations.

---

Rename layer
Share
Mouse over the calculation you want to share with the organization members and click Share calculation
task button.
Delete
Deletes the calculation from the Prediction History widget.
3.1.6 Antennas
Click this button to open Antennas tool.
Preview the list of available antennas in the project. The antennas are used for point-to-area calculations.

Search
Initiates the search procedure in the antennas list.
Delete antenna
Delete antenna using Delete button.
Click on an antenna to preview the antenna patterns.

Adjust vertical pattern
In the case where you have an electrically tilted vertical antenna pattern imported, you might want to tilt it
back so it is essentially a 0 tilt antenna pattern (recommended if you use electrical tilt field in cell attributes).
You may use the adjust vertical pattern tool to do this. Find the center of the main lobe of the vertical
antenna pattern using the “main lobe center” slider, then click accept.

3.1.6.1 Import Antennas
To import new antennas, click the New Antenna button
and then select Import Files.
To start the import procedure, select or drag and drop the antenna pattern file. Planet format antenna
pattern files are supported. Here is an example:

3.1.6.1 Import HCM code file
To import HCM code patterns as antennas, you may use this import option. The required file is a CSV with
3 fields, antenna gain, horizontal HCM code and vertical HCM code. These are then combined and imported
as antenna patterns under the HCM manufacturer group. Multiple lines are allowed.
CSV file example:
After file upload, you are prompted to assign which CSV field corresponds to the required parameters:
3.1.6.2 Import cell array antenna
If you have separate pattern files for a multibeam antenna, you may use this import option to combine them
into a single cell array antenna pattern.

Antenna parameters
Manufacturer
Antenna manufacturer.
Model
Antenna name.
Frequency
Antenna frequency value in MHz.
Gain
Antenna gain value in dBi.

3.1.6.3 Create manually
To manually create an antenna, click the New Antenna button
and then select Create Manually.

Antenna parameters
Manufacturer
Antenna manufacturer (company or entity).
Model
Antenna name.

Frequency
Antenna frequency value in MHz.
Gain
Antenna gain value in dBi.
Max attenuation
Attenuation value assigned to the attenuated parts of the antenna pattern
Horizontal pattern
Beamwidth
Antenna’s horizontal beamwidth value in degrees. Used for generating the antenna pattern.
Smoothing degree count
Transition width between attenuated and non-attenuated parts of the antenna pattern in degrees. The
attenuation values are linearly interpolated between 0 and the max attenuation value within this transition
range.
Vertical pattern
Beamwidth
Antenna’s vertical beamwidth value in degrees. Used for generating the antenna pattern.
Smoothing degree count
Transition width between attenuated and non-attenuated parts of the antenna pattern in degrees. The
attenuation values are linearly interpolated between 0 and the max attenuation value within this transition
range.
Angle offset
Transition width between attenuated and non-attenuated parts of the antenna pattern in degrees. The
attenuation values are linearly interpolated between 0 and the max attenuation value within this transition
range.
Mirror pattern
Ability to mirror the vertical attenuation pattern.
Pattern preview
