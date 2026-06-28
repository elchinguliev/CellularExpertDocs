# 05. __S0__

Modelling Outdoor coverage
The CE tools make use of three distinct [GIS](https://www.google.com/search?q=GIS+Geographic+Information+System) data layers to obtain high
precision modelling of radio [wave propagation]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=radio+wave+propagation+physics) losses:
1. [Digital [Terrain]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography) Model](https://www.google.com/search?q=Digital+[Terrain](https://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography)+Model+[DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation+data)+bare+earth) ([DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model)), also known as Digital [Elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum)
Model ([DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain)), which describes Earth surface, i.e., path terrain
profile in terms of ground [elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum) above uniform sea level.
2. Obstacles layer, delineating buildings and other such objects
above Earth surface that may be considered to be principal
impediments for radio [wave propagation](https://www.google.com/search?q=radio+wave+propagation+physics).
3. [Clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) layer, delineating natural occurring or human cultivated
ground cover that may be partially penetrable by radio waves,
such as natural vegetation (e.g., forests, trees, bushes) or various
crops, gardens, parks, etc.
[Diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation) Free Space Loss
[Diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation)
H
obstacles
H
[Clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) losses [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio) [DSM](https://www.google.com/search?q=DSM+Digital+Surface+Model)
UE
[DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation+data)

---

Point to point (Profile) input
- Geodata
- Elevation
- Buildings
- Clutter
- Frequency
- [Fresnel zone](https://www.google.com/search?q=Fresnel+zone+radio+link+clearance) (%)
- Earth radius
- Transmitter
- Height
- Power
- Receiver
- Height
- Power

---

Profile calculations
- General
- Clearance
- Clearance Percentage
- Clearance Distance
- Distance to [NLOS](https://www.google.com/search?q=NLOS+Non+Line+of+Sight+radio+propagation)
- Distance to OLOS
- Power Budget
- Downlink FS
- Uplink FS
- FWA downlink RSL
- FWA uplink RSL
- [Path Loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit))
- Total [Path Loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit))
- Model Loss
- Diffraction Loss
- Penetration Loss
- Receiver Clutter Loss
- Clutter Loss
- Angles

---

Dynamic profile
- Fix transmitter
- Dynamic option

---

Profile symbology
- Define colors for each object in profile

---

Profile 3D

---

Profile 3D

---

Visibility prediction input
- Geodata
- Elevation
- Obstacle
- Frequency
- Calculation radius
- Earth radius
- Transmitter
- Receiver (height)

---

Visibility Results
- [Line of Sight](https://www.google.com/search?q=Line+of+Sight+[LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation)+radio+propagation)
- Required height for [LoS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation)
- Clearance

---

Visibility: [Line of Sight](https://www.google.com/search?q=Line+of+Sight+LOS+radio+propagation)
Possible values:
- 0
- 1

---

Visibility: Clearance
- Clearance – clearance of visibility line between Tx to Rx as a distance in
meters
Height, m
Clearance = 6.5 m
0 100 200 300 400Distance, m

---

Visibility: Minimum Receiver Height
- Receiver height – calculate required receiver heights to have a visibility

---

Visibility: Line of Sight sum meter topo data

---

Surface vs Eelevation+Obstacles
T
T
x
x
V
V
is ib le
R
is ib le
R x
x
N
V
o
is ib
t v is
le
ib
R
R x
le
x
S
O
E
u rfa c e g rid
b s ta c le s g rid
le v a tio n g rid

---

Surface

---

DTM + Obstacles (Buildings/Vegetation)

---

DTM + Buildings + Vegetation

---

Exercise
Description: C:\CE_Course\0. Descriptions
Name: 2. Line of Sight (Profile).pdf

---

Thank you!
Tel.: +370 5 2150575
Email: info@cellular-expert.com
S.Konarskio g. 28A LT-03127 Vilnius
Lithuania
www.cellular-expert.com

---
