# 05. Line of Sight

Modelling Outdoor coverage
The CE tools make use of three distinct GIS data layers to obtain high
precision modelling of radio wave propagation losses:
1. Digital Terrain Model (DTM), also known as Digital Elevation
Model (DEM), which describes Earth surface, i.e., path terrain
profile in terms of ground elevation above uniform sea level.
2. Obstacles layer, delineating buildings and other such objects
above Earth surface that may be considered to be principal
impediments for radio wave propagation.
3. Clutter layer, delineating natural occurring or human cultivated
ground cover that may be partially penetrable by radio waves,
such as natural vegetation (e.g., forests, trees, bushes) or various
crops, gardens, parks, etc.
Diffraction Free Space Loss
Diffraction
H
obstacles
H
Clutter losses clutter DSM
UE
DTM
2


---

Point to point (Profile) input
•
Geodata
•
Elevation
•
Buildings
•
Clutter
•
Frequency
•
Fresnel zone (%)
•
Earth radius
•
Transmitter
•
Height
•
Power
•
Receiver
•
Height
•
Power
3


---

Profile calculations
•
General
•
Clearance
•
Clearance Percentage
•
Clearance Distance
•
Distance to NLOS
•
Distance to OLOS
•
Power Budget
•
Downlink FS
•
Uplink FS
•
FWA downlink RSL
•
FWA uplink RSL
•
Path Loss
•
Total Path Loss
•
Model Loss
•
Diffraction Loss
•
Penetration Loss
•
Receiver Clutter Loss
•
Clutter Loss
•
Angles
4


---

Dynamic profile
• Fix transmitter
• Dynamic option
5


---

Profile symbology
• Define colors for each object in profile
6


---

Profile 3D
7


---

Profile 3D
8


---

Visibility prediction input
• Geodata
• Elevation
• Obstacle
• Frequency
• Calculation radius
• Earth radius
• Transmitter
• Receiver (height)
9


---

Visibility Results
• Line of Sight
• Required height for LoS
• Clearance
10


---

Visibility: Line of Sight
Possible values:
• 0
• 1
11


---

Visibility: Clearance
• Clearance – clearance of visibility line between Tx to Rx as a distance in
meters
Height, m
Clearance = 6.5 m
75
70
65
60
55
0 100 200 300 400Distance, m
12


---

Visibility: Minimum Receiver Height
• Receiver height – calculate required receiver heights to have a visibility
13


---

Visibility: Line of Sight sum meter topo data
14


---

Surface vs Eelevation+Obstacles
15
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
16


---

DTM + Obstacles (Buildings/Vegetation)
17


---

DTM + Buildings + Vegetation
18


---

Exercise
Description: C:\CE_Course\0. Descriptions
Name: 2. Line of Sight (Profile).pdf
19


---

Thank you!
Tel.: +370 5 2150575
Email: info@cellular-expert.com
S.Konarskio g. 28A LT-03127 Vilnius
Lithuania
www.cellular-expert.com


---
