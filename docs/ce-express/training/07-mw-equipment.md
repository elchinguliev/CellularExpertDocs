# 07. MW Equipment

1. Objective
This tutorial will show you how to add new MW links, manage and do predictions.
At the end of the exercise you will be able to:
- Create and [import]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=data+import+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) MW equipment.
- Create MW links in the project.
- Do MW Predictions.
2. Initial data
Prepared project with:
- Geodata.
- Equipment and models.
3. Manage MW equipment
Navigate to C:\CE_Course\MW_Equipment\Project and run Project.aprx file to open the
prepared project for RL Introduction exercise.
[Microwave]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning) links involve additional equipment settings compared to point-to-area predictions.
These settings include frequency plans, radio equipment, and parabolic antennas, which are
used for predicting power budget, [interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent), or [availability](https://www.google.com/search?q=link+availability+percentage+[microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning)+ITU). In this section, we will cover
how to create and, if necessary, [import](https://www.google.com/search?q=data+import+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) this data into the project.

## 3.1 Parabolic antennas

Open Antenna Viewer in CE RLP tab, and change antenna type from [Sector](https://www.google.com/search?q=[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+sector+antenna+coverage+area) to Parabolic.
All parabolic antennas will be displayed.

---

Close Antenna Viewer tool. To import a new parabolic antenna, open Import/[Export](https://www.google.com/search?q=data+export+GIS+raster+vector) Antenna
Files tool. Parabolic antenna import supports:
- Andrew format:
- NSMA format:

---

Select Parabolic (NSMA Format).
Click on Select Antenna Model Files
Browse to C:\CE_Course\RL_Prediction\Equipment\Antennas, select Antenna10GHz.txt file
and press OK button. It will appear in Import/[Export](https://www.google.com/search?q=data+export+GIS+raster+vector) Antenna Files dialog.
Select Check box near the antenna and press Import Antennas button.

---

Antenna will be imported successfully. Now choose Andrew format.
Click on Select Antenna Model Files
Browse to C:\CE_Course\RL_Prediction\Equipment\Antennas, select a2119.adf antenna
and press OK button to add it.
Select Check box near the antenna and press Import Antennas button.
Now open Antenna Viewer tool to review these antennas.

---

Close Antenna Viewer and Import tools.

## 3.2 Radios

This equipment category encompasses details about radio transceivers utilized in microwave
links. It comprises information on transmitter power, receiver [sensitivity](https://www.google.com/search?q=receiver+sensitivity+[dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit)+radio), [noise figure](https://www.google.com/search?q=noise+figure+receiver+[sensitivity](https://www.google.com/search?q=receiver+sensitivity+[dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit)+radio)+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit)),
nonlinearity characteristics, and maximum data [capacity](https://www.google.com/search?q=network+capacity+planning+telecom).
Open Radios tool in CE RLP tab and preview available Radio within default CE [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase).

---

It has parameter section, and Modulations section.
Click on Add button in top right corner of the dialog.
Define the same parameters as defined below:
- Model: RL Radio
- Manufacture: CE

---

- Frequency From, [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit): 9500
- Frequency To, [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit): 10500
- [Bandwidth](https://www.google.com/search?q=channel+bandwidth+radio+frequency+MHz), MHz: 10
- MTBF, h: 300000
- MTTR, h: 24
- Bit Rate, kbps: 2048
- Block Size, bits: 2048
- Burst Errors: 1
- Dispersive [Fade Margin](https://www.google.com/search?q=fade+margin+link+budget+microwave+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit)), dB: 50
- BER 10-3 Threshold, dBm: -76
- BER 10-6 Threshold, dBm: -72
- [Noise Figure](https://www.google.com/search?q=noise+figure+receiver+sensitivity+dB), dB: 5
- Residual BER: 1E-12
- IIP2, dBm: 30
- IIP3, dBm: 29
- XPIF, dB: 20
- Power, dBm: 20
- Power Low, dBm: 10
- Power High, dBm: 26
- Automatic Transfer Power Control Range, dB: 20

---

Click on Modulations tab, and include these modulations:
You can do it simply selecting modulation from the list and press + button to add it for the
radio.
Each modulation has its own default parameters.

---

Leave default parameters and press Create button. The new radio will be added in the list.
Click on Import tab.
Click on Seleted Data File and navigate to C:\CE_Course\MW_Equipment\Equipment\Radio,
select Aur24_1E1.raf and press OK button.

---

New radio with the parameters will be added to the dialog. Press Import button to import it
to the database.
Close Radio tool.

## 3.3 Frequency plans

Frequency planning is important for microwave link design, optimizing [spectrum](https://www.google.com/search?q=radio+frequency+spectrum+allocation+telecom) use, and
preventing [interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent). By strategically allocating frequency bands, it enhances efficiency,
complies with regulations, and coordinates with other services. This planning considers
propagation characteristics and facilitates scalability, ensuring optimal performance for
microwave links in various environments and supporting future technology upgrades.
Frequency plans can be imported from a text file, or created manually.
3.3.1 Create manually
Open Frequency Plans tool in CE RLP tab.

---

Click on Add section and define:
- Frequency Plan Name: FP 10MHz 8 Carriers
- Low Frequency, MHz: 9800
- Carrier Spacing, MHz: 50
- Duplex Spacing, MHz: 300
- Carriers: 8
High Frequency, MHz will be filled automatically.
Press Add Frequency Plan button.
The new frequency plan will appear in the main dialog.
3.3.2 Import
Click on Import option, and then on Select Data Files.

---

Navigate to C:\CE_Course\RL_Prediction\Equipment\FrequencyPlans, select all files and
press OK button.
Frequency Plans will be added to the preview.

---

Press Import button and they will be imported to the database.
Close Frequency Plans dialog.

---
