# 05. Import Data

1. Objective
This module explains how to [import]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=data+import+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) external data into [CE Express]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) and how imported data
becomes part of the project environment. It covers the [import](https://www.google.com/search?q=data+import+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) of [network objects](https://www.google.com/search?q=radio+network+objects+sites+cells+GIS) from CSV
files and antenna patterns from external files, as well as the use of mapping templates to
ensure consistency and repeatability.
By the end of this exercise, participants will be able to:
- Import [network objects](https://www.google.com/search?q=radio+network+objects+sites+cells+GIS) using CSV files
- Map external data fields to [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) object attributes
- Create and reuse import mapping templates
- Import [antenna pattern](https://www.google.com/search?q=antenna+radiation+pattern+format) files into the CE Express database
- Verify and review imported data within the [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase)
2. Understanding Data Import in CE Express
Data import is a key capability in CE Express, allowing users to bring information from
external sources into a [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase). Imported data may originate from:
- External planning tools
- Inventory systems
- Field surveys
- Desktop-based CE projects
CE Express supports structured import workflows to ensure that imported data is:
- Correctly mapped to internal object models
- Consistent across multiple imports
- Easy to review and validate after import
3. Initial Data and Prerequisites
This exercise assumes:

---

- A prepared workspace created in previous exercises
- Prepared geodata loaded in the workspace
- Access to import files stored locally on the computer
4. Exercise

## 4.1 Step 1 – Open the Workspace

1. Open the CE Express application:
https://cecom2.cellular-expert.com/ce_express/
2. From the workspace list, select the workspace used in the previous exercise.

## 4.2 Step 2 – Importing Network Objects (Cells and Sites)

4.2.1 Purpose of [Network Object](https://www.google.com/search?q=radio+network+object+GIS+database) Import
Importing network objects allows users to rapidly populate a workspace with sites and cells
instead of creating them manually. This approach is especially useful when working with
existing datasets or migrating data between systems.
4.2.2 Opening the Import Tool
1. Open the Features tool.
2. Click Import Features.
3. Select Cells.

---

The Import dialog opens on the right side of the screen.
4.2.3 Loading the CSV File
1. Open Windows File Explorer.
2. Navigate to:
C:\CE_Course\ImportingData\Network
3. Select the file Cells_CE_Express.csv.
4. Drag and drop the file into the Import dialog.
The CSV file is uploaded and ready for mapping.
4.2.4 Defining Import Options
Enable the following options:
- Create Sites – automatically creates [site](https://www.google.com/search?q=cell+site+tower+base+station+location) objects based on [site](https://www.google.com/search?q=cell+site+tower+base+station+location)-related fields

---

- Use Mapping – allows explicit mapping between CSV fields and CE Express
attributes
These options ensure that both sites and cells are created correctly during import.
4.2.5 Mapping CSV Fields to CE Express Attributes
Mapping defines how columns in the CSV file are translated into CE Express object
parameters.
For each attribute, define the following mappings:
CE Express CSV file Fill
[Cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) name [Cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) Name Leave empty
X longitude Leave empty
Y latitude Leave empty
[Azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north) [Azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north) Leave empty
Site name Tower Name Leave empty
Height [Height Above Ground](https://www.google.com/search?q=height+above+ground+[AGL](https://www.google.com/search?q=AGL+Above+Ground+Level+height+measurement)+antenna) Leave empty
[Downtilt](https://www.google.com/search?q=antenna+downtilt+mechanical+electrical+degrees) Tilt Leave empty
El. [Downtilt](https://www.google.com/search?q=antenna+downtilt+mechanical+electrical+degrees) Leave empty 0
Frequency Frequency Leave empty
Power Cell Power Leave empty
Misc loss, [dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit) Leave empty 0
[Bandwidth](https://www.google.com/search?q=channel+bandwidth+radio+frequency+[MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit)) [Bandwidth](https://www.google.com/search?q=channel+bandwidth+radio+frequency+[MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit)) Leave empty
[Noise figure](https://www.google.com/search?q=noise+figure+receiver+[sensitivity](https://www.google.com/search?q=receiver+sensitivity+[dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit)+radio)+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit)) Leave empty 6
Downlink duplex factor Leave empty 0.6
[Subcarrier spacing](https://www.google.com/search?q=[subcarrier](https://www.google.com/search?q=subcarrier+spacing+[OFDM](https://www.google.com/search?q=OFDM+Orthogonal+Frequency+Division+Multiplexing)+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+[4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)+mobile)+[5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network))+spacing+[OFDM](https://www.google.com/search?q=OFDM+Orthogonal+Frequency+Division+Multiplexing)+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+[4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)+mobile)+[5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network)+[kHz](https://www.google.com/search?q=kHz+kilohertz+frequency+unit)) Leave empty 30

---

TX [MIMO](https://www.google.com/search?q=MIMO+Multiple+Input+Output+antenna) TxMIMO Leave empty
[RX MIMO](https://www.google.com/search?q=Rx+[MIMO](https://www.google.com/search?q=MIMO+Multiple+Input+Multiple+Output+antenna+technology)+receive+antenna+configuration) RxMIMO Leave empty
Active antenna effect Leave empty 6
Cell load, % Leave empty 30
Color index Leave empty Leave empty
Technology Tech Leave empty
Prediction model ID Leave empty 3
Prediction model configuration ID Leave empty 4
Frequency group frequency_group Leave empty
antenna_id Leave empty 515
carriers Leave empty []
site_id Leave empty Leave empty
duplex_mode Duplex Leave empty

---

4.2.6 Saving a Mapping Template
Before importing, save the mapping configuration:
1. In Mapping presets, click + New mapping preset.
2. Enter the template name:
Import template
3. Click Apply to save the preset.
Using mapping templates ensures consistency and avoids repeating manual configuration
for future imports.
4.2.7 Importing the Data
1. Click Accept to start the import.
2. Wait until the import process completes.
3. Close the Import tool.

---

4.2.8 Verifying Imported Objects
1. Ensure the Features tool is active.
2. Click once on the map to select imported objects.
3. Review the objects listed in the Features panel.
This confirms that cells and sites were successfully created and loaded into the workspace.

---

## 4.3 Step 3 – Importing Antenna Patterns

4.3.1 Purpose of Antenna Import
Antenna patterns define how energy is distributed spatially. Importing accurate antenna
patterns ensures that predictions and analyses reflect real equipment behavior.
4.3.2 Reviewing the Antenna File
1. Navigate to:
C:\CE_Course\ImportingData\Antenna
2. Open the file ADU4518R6v06_2655.txt using Notepad.
The file is in Planet format and contains:
- Header information
- Horizontal [radiation pattern](https://www.google.com/search?q=antenna+radiation+pattern+horizontal+vertical)
- Vertical [radiation pattern](https://www.google.com/search?q=antenna+radiation+pattern+horizontal+vertical)
This format is supported for direct import into CE Express.
4.3.3 Importing the Antenna File
1. Open the Antennas tool.

---

2. Click + New Antenna.
3. Click Import files.
4. Drag and drop the antenna text file into the import area.
The antenna is automatically added to the CE Express antenna database.

## 4.4 Reviewing Imported Antenna Data

1. Select the imported antenna from the list.
2. Review antenna properties and radiation patterns.
Verifying antenna data ensures it is ready for assignment to cells and use in predictions.

---

3. Close the Antennas tool.
5. Summary and Key Takeaways
- Data import enables rapid population of workspaces using external datasets
- CSV import with explicit mapping ensures correct parameter assignment
- Mapping templates provide repeatability and consistency
- [Antenna pattern](https://www.google.com/search?q=antenna+radiation+pattern+file+format+MSI) import allows use of real equipment characteristics
- Verifying imported data is essential before running predictions or further analysis

---
