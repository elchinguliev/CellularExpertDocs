# 02. Architecture

CE Products and Solutions
[CE Desktop]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Desktop+[ArcGIS]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+Pro) [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform)
For [ArcGIS Pro](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+Pro+Esri+desktop+software) For [ArcGIS Enterprise](https://www.google.com/search?q=ArcGIS+Enterprise+server+GIS)
- Desktop, Single Use [Radio Planning](https://www.google.com/search?q=radio+network+planning+telecom) system • Web-based [Radio Planning](https://www.google.com/search?q=radio+network+planning+telecom) system
- Wireless planning tools, together with • Server-based, Multi User system
[ArcGIS Pro](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+Pro+Esri+desktop+software) functionality • Includes CE [Inventory3D](https://www.google.com/search?q=Cellular+Expert+Inventory3D+asset+management)
- Can be used as a client of [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) system • Dashboard of Network Coverage Statistics
CE Customized solutions
ArcGIS CE COTS

---

[CE Pro](https://www.google.com/search?q=Cellular+Expert+CE+Pro+ArcGIS+planning)

---

Cellular Expert for [ArcGIS Pro](https://www.google.com/search?q=ArcGIS+Pro+Esri+desktop+software) Architecture
Cellular Expert for ArcGIS Pro
RCP | RLP | [EMF](https://www.google.com/search?q=EMF+electromagnetic+field+exposure+assessment)
Basic or higher license
ArcGIS Pro 3.1 and
above
Additional extensions are not
required
Local Database All files are saved in local disk

---

Cellular Expert for ArcGIS Pro
License Structure
- RCP – Radio [Coverage Prediction](https://www.google.com/search?q=coverage+prediction+RF+radio+planning)
- RLP – [Radio Link](https://www.google.com/search?q=radio+link+[microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning)+point+to+point) Prediction
- [EMF](https://www.google.com/search?q=EMF+electromagnetic+field+exposure+assessment) – [Electromagnetic Field](https://www.google.com/search?q=electromagnetic+field+EMF+exposure+limits)

---

Geospatial Information
✓ Field measurements
✓ Network coverage
✓ Network data
✓ Demography
✓ [Land cover](https://www.google.com/search?q=land+cover+classification+satellite+imagery) / use
✓ Obstacles
✓ [Elevation](https://www.google.com/search?q=elevation+model+[terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography)+height+datum)
✓ Surface

---

Project files
Project > Save Project/Save Project As

---

Cellular Expert Project Structure
- Predictions
- Results
- SystemFiles
- Temp
- VolatileResults
- VolatileTemp
- [Workspace](https://www.google.com/search?q=ArcGIS+workspace+project+geodatabase).gdb

---

[Workspace](https://www.google.com/search?q=ArcGIS+workspace+project+geodatabase) database files

---

Environment
- Geographic data
- Cellular Expert Workspace
- Results

---

Cellular Expert Workspace

---

Inside Workspace
➢ Network Data
➢ Equipment Data
➢ Modelling Settings

---

Network Data Structure
[RF prediction](https://www.google.com/search?q=RF+radio+frequency+prediction+coverage) does not require [Site](https://www.google.com/search?q=cell+site+tower+base+station+location)
object. Cells can be created
[Cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) – logical
without [Site](https://www.google.com/search?q=cell+site+tower+base+station+location) object.
information
Cells
about [sector](https://www.google.com/search?q=[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+sector+antenna+coverage+area):
Cell still has SiteID value, which
a set of channels can be define in the attributes.
SiteID is used for Carrier
Aggregation.
Site and Cell is connected through
Site – location point with
SiteID value.
unique identifier:
Site [Base station](https://www.google.com/search?q=base+station+[BTS](https://www.google.com/search?q=BTS+Base+Transceiver+Station+GSM+[2G](https://www.google.com/search?q=2G+GSM+mobile+network+second+generation))+[NodeB](https://www.google.com/search?q=NodeB+[3G](https://www.google.com/search?q=3G+UMTS+HSPA+mobile+network)+[UMTS](https://www.google.com/search?q=UMTS+[3G](https://www.google.com/search?q=3G+UMTS+HSPA+mobile+network)+Universal+Mobile+Telecommunications)+base+station)+[eNodeB](https://www.google.com/search?q=eNodeB+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+[4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)+mobile)+[4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)+base+station)+[gNodeB](https://www.google.com/search?q=gNodeB+[5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network)+NR+base+station)) SiteID must be Integer.
Site name is defined for Site object.
Cells

---

Cell
➢ 800 [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit)
➢ 1800 [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit)
➢ 2100 MHz

---

Site

---

Antenna

---

CE [Path Loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit)) models (10kHz - 350 [GHz](https://www.google.com/search?q=GHz+gigahertz+frequency+unit))
1. CEC [ITU-R](https://www.google.com/search?q=ITU+R+radio+communication+standard) Model (100MHz – 6GHz) is a combination model intended for use in a variety of different radiocommunication systems which is derived explicitly
from [ITU-R](https://www.google.com/search?q=ITU+R+International+Telecommunication+Union+Radio) [path loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation) modelling methods as follows:
a. Receive antenna in [LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation) condition – [path loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit)) calculated as FSL based on Recommendation [ITU-R](https://www.google.com/search?q=ITU+R+International+Telecommunication+Union+Radio) P.525 (ref URL);
b. Receive antenna in OLOS condition – total path loss modelled as a combination of basic FSL calculated based on Recommendation ITU-R P.525 (ref
URL) and [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio) loss calculated based on Recommendation ITU-R P.2108 (ref URL);
c. Receive antenna in [NLOS](https://www.google.com/search?q=NLOS+Non+Line+of+Sight+radio+propagation) condition – path loss as a combination of basic FSL calculated based on Recommendation ITU-R P.525 (ref URL), additional
losses due to [diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation) calculated based on Recommendation ITU-R P.526 (ref URL) and the [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) losses calculated based on Rec. ITU-R P.2108
(ref URL).
2. ITU-R P.452 Model (6GHz – 50GHz) is provided as a universally applicable model with very wide frequency range from 0.1-50 [GHz](https://www.google.com/search?q=GHz+gigahertz+frequency+unit). Its implementation is
based on the methodology described in the Recommendation ITU-R P.452 (ref URL). This model does not provide for definition of OLOS visibility condition;
instead it considers [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) as part of general obstacles category and accordingly distinguishes only two radio visibility cases:
a. Receive antenna in [LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation) condition – path loss modelled based on FSL principle;
b. Receive antenna in [NLOS](https://www.google.com/search?q=NLOS+Non+Line+of+Sight+radio+propagation) condition – total path loss modelled using a combination of basic transmission losses and losses due to [diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation).
3. LOS ITU-R P.525 Model (6GHz – 100GHz) is the FSL path loss calculated based on method in Recommendation ITU-R P.525 (ref URL). As such it could be
used for modelling of radio links where LOS is considered a necessary condition, e.g., for Fixed ([Point-to-Point](https://www.google.com/search?q=point+to+point+radio+link+[microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning))) Links or Mobile Systems in mmWave bands.
4. UniMacro Model (400MHz – 3GHz) is the CE’s proprietary combination model developed over the years of practical experience with the operational planning
of cellular mobile networks in the frequency ranges from 400-2600 MHz. It had been fine tuned to produce coverage predictions that are most closely aligned
with what could be expected to be experienced by the actual mobile network users in the field. The model will model different path losses depending on radio
visibility conditions as follows:
a. Receive antenna in LOS condition – path loss modelled based on FSL principle;
b. Receive antenna in OLOS condition – path loss modelled using Extended Hata (Open Area) model with additional clutter loss calculated based on
Recommendation ITU-R P.2108 (ref URL);
c. Receive antenna in NLOS condition – path loss modelled using Extended Hata model with additional losses due to diffraction calculated based on
Recommendation ITU-R P.526 (ref URL) as well as clutter losses based on Rec. ITU-R P.2108 (ref URL).
5. ITU-R P.368 Model (10kHz – 30MHz)

---

CE prediction models

---

Other

---
