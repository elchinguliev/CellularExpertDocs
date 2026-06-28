# 08. MW Prediction

1. Objective
This tutorial will show you how to add new MW links, manage and do predictions.
At the end of the exercise you will be able to:
- Create and [import]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=data+import+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) MW equipment.
- Create MW links in the project.
- Do MW Predictions.
2. Initial data
Prepared project with:
- [Network objects]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=radio+network+objects+sites+cells+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)).
- Geodata.
- Equipment and models.
3. Add Links
The link objects can be imported or created manually using Add functionality. Open Add
Object tool and select Link option from drop-down menu list.

---

Click once on T1 [site](https://www.google.com/search?q=cell+site+tower+base+station+location) and second time to D1 [site](https://www.google.com/search?q=cell+site+tower+base+station+location).
It will fill general parameters automatically.
Height, [azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north) and other parameters are calculated automatically, leave them as it is.
Press Show Profile button to preview topographical data between Site A and Site B, if there
is [LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation), what [Fresnel zone](https://www.google.com/search?q=Fresnel+zone+radio+link+clearance) percentage value, etc.
Profile will be generated.

---

Close Profile windows.
Define parameters are defined below:
- Name: MW001
- Radio Model: 2. Aurora 2400
- Frequency Plan: 10GHz-CEPT12-05-3_5MHz-350MHz
- Carriers: 1 and 3 (1’ and 3’ will be automatically assigned).
- Go to Antenna section and change antenna to Antenna 10MHz

---

Press Save Changes button.
Do not close the dialog, create new links and define parameters:
- Between D1 and E2
o Name: MW002
o SiteA: Lower
o Radio Model: 2. Aurora 2400
o Frequency Plan: 10GHz-CEPT12-05-3_5MHz-350MHz

---

o Carriers: 2 and 4
o Antenna for Site A and Site B: Antenna 10MHz
Press Save Changes
- Between E6 and M77
o Name: MW003
o SiteA: Lower
o Radio Model: 2. Aurora 2400
o Frequency Plan: 10GHz-CEPT12-05-3_5MHz-350MHz
o Carriers: 1 and 4

---

o Antenna for Site A and Site B: Antenna 10MHz
Press Save Changes
4. RL Predictions
The predictions are working between selected links and provides all necessary information
about power budget, [interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent) or [availability](https://www.google.com/search?q=link+availability+percentage+[microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning)+ITU).
Select all links on the map and open Link Prediction tool. Before launching the predictions,
enable Calculate [Interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent) option.

---

Press Run button and wait will prediction are completed and results loaded into your project.
The primary results are Power Budget and Profile between Tx and Rx. On the left, select
another link and results will be updated accordingly.

---

Selected Link can have several carriers, to preview the results expand Carrier option.
Click on Interference tab to display interfering links and interfered links information.
Total Interference is shown in Power Budget section.
Interference link predictions can be previewed too. Click on Interfering Link in top left corner
and it will display selected interfering link Power Budget, [Path Loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit)) and draw a line on the
map.

---

Go back to Links section, select MW001 from T1 to D1, Carrier 1’H.
Click on Interference tab, and analize Inteference From table. Link MW002, from Site: E2
with Carrier 2’H interferes:
- Interference, [dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit): -100.248 [dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit)
- FML, [dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit): 1.29E-10
Close Link Prediction results, select MW002 link on the map and open Object Editor.
Double click on the link.

---

Find Frequency Plan table, select Upper and change carrier 2’ polarization to Vertical.
Save Changes.
Select all links on the map, open Link Prediction tool again and run predictions.
After predictions are done, open MW001 (A-B) interference predictions and preview how
Interference From is changed for MW002 link, Site E2.
Close Link Prediction Results dialog.

## 4.1 Geoclimatic data

[Geoclimatic](https://www.google.com/search?q=geoclimatic+factor+[microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning)+fading+ITU) data, comprising factors such as rain rate, temperature, [gaseous absorption](https://www.google.com/search?q=gaseous+[absorption](https://www.google.com/search?q=atmospheric+absorption+radio+signal)+oxygen+water+vapour+radio),
and [multipath fading](https://www.google.com/search?q=multipath+fading+radio+propagation), significantly shapes the planning and efficacy of microwave links.
Rain rate introduces the challenge of [rain fade](https://www.google.com/search?q=rain+fade+attenuation+microwave), where increased rainfall leads to greater
signal [attenuation](https://www.google.com/search?q=signal+attenuation+loss+radio+propagation). To address this, microwave link planners employ [rain attenuation](https://www.google.com/search?q=rain+[attenuation](https://www.google.com/search?q=signal+attenuation+loss+radio+propagation)+microwave+ITU+R+P838)
models, adjusting transmitter power or incorporating diversity techniques to maintain link
reliability. Temperature variations impact atmospheric conditions, influencing signal
propagation. Planners consider these effects to optimize link performance and account for
temperature-related changes in their designs. [Gaseous absorption](https://www.google.com/search?q=gaseous+[absorption](https://www.google.com/search?q=atmospheric+absorption+radio+signal)+oxygen+water+vapour+radio), particularly by
atmospheric water vapor and oxygen, is factored into link planning by selecting frequency
bands less susceptible to absorption, particularly for long-distance links. Lastly, the impact
of [multipath fading](https://www.google.com/search?q=[multipath](https://www.google.com/search?q=multipath+propagation+fading+radio)+fading+radio+propagation+effect) is mitigated through strategies like antenna diversity and adaptive
modulation, as well as [terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography)-aware antenna placement. By navigating these [geoclimatic](https://www.google.com/search?q=geoclimatic+factor+microwave+fading+ITU)
challenges, microwave link planners ensure robust and effective communication links in
diverse environmental conditions.
The tool is located in CE RLP tab, Radio Links section.

---

Run Link Predictions again. After successful calculations, leave MW001 (A-B) link selected,
and click on Performance tab.
Review [Multipath](https://www.google.com/search?q=multipath+propagation+fading+radio) ITU and Rain ITU percentage values.
Close results, and open Geoclimatic Data tool.
Click on [Multipath Fading](https://www.google.com/search?q=multipath+fading+radio+propagation+effect) tab, and define:
- [ITU-R P.530](https://www.google.com/search?q=ITU+R+P530+microwave+fading) version: 17

---

Click on Rain Fading tab, and define:
Press Save Changes. Close Geoclimatic Data tab, and run Link Predictions again. Review
Performance tab calculations for MW001 (A-B) link. Compare them with previous results.

---
