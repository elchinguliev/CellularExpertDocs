# 08. Prediction Models

[Path Loss]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=path+loss+radio+signal+attenuation+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit))
𝐹𝑖𝑒𝑙𝑑 𝑆𝑡𝑟𝑒𝑛𝑔ℎ𝑡 = 𝐸𝐼𝑅𝑃 − 𝐴𝑛𝑡𝑒𝑛𝑛𝑎𝐴𝑡𝑡𝑒𝑛𝑢𝑎𝑡𝑖𝑜𝑛 -
PathLoss

---

Prediction Models
- [ITU-R](https://www.google.com/search?q=ITU+R+radio+communication+standard) P.452 (6GHz to 50GHz)
- UniMacro (400MHz to 3GHz)
- CEC [ITU-R](https://www.google.com/search?q=ITU+R+International+Telecommunication+Union+Radio) (100MHz to 6GHz)
- [LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation) [ITU-R](https://www.google.com/search?q=ITU+R+International+Telecommunication+Union+Radio) P.525 (6GHz to 100 [GHz](https://www.google.com/search?q=GHz+gigahertz+frequency+unit))
- ITU-R P.368 (10kHz to 30MHz)

---

CE [Path Loss]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=path+loss+radio+signal+attenuation+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit)) models (10kHz - 100 [GHz](https://www.google.com/search?q=GHz+gigahertz+frequency+unit))
1. CEC ITU-R Model (100MHz – 6GHz) is a combination model intended for use in a variety of different radiocommunication systems which is derived explicitly
from ITU-R [path loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation) modelling methods as follows:
a. Receive antenna in [LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation) condition – path loss calculated as FSL based on Recommendation ITU-R P.525 (ref URL);
b. Receive antenna in OLOS condition – total path loss modelled as a combination of basic FSL calculated based on Recommendation ITU-R P.525 (ref
URL) and [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio) loss calculated based on Recommendation ITU-R P.2108 (ref URL);
c. Receive antenna in [NLOS](https://www.google.com/search?q=NLOS+Non+Line+of+Sight+radio+propagation) condition – path loss as a combination of basic FSL calculated based on Recommendation ITU-R P.525 (ref URL), additional
losses due to [diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation) calculated based on Recommendation ITU-R P.526 (ref URL) and the [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) losses calculated based on Rec. ITU-R P.2108
(ref URL).
2. ITU-R P.452 Model (6GHz – 50GHz) is provided as a universally applicable model with very wide frequency range from 0.1-50 GHz. Its implementation is
based on the methodology described in the Recommendation ITU-R P.452 (ref URL). This model does not provide for definition of OLOS visibility condition;
instead it considers [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) as part of general obstacles category and accordingly distinguishes only two radio visibility cases:
a. Receive antenna in LOS condition – path loss modelled based on FSL principle;
b. Receive antenna in [NLOS](https://www.google.com/search?q=NLOS+Non+Line+of+Sight+radio+propagation) condition – total path loss modelled using a combination of basic transmission losses and losses due to [diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation).
3. LOS ITU-R P.525 Model (6GHz – 100GHz) is the FSL path loss calculated based on method in Recommendation ITU-R P.525 (ref URL). As such it could be
used for modelling of radio links where LOS is considered a necessary condition, e.g., for Fixed ([Point-to-Point](https://www.google.com/search?q=point+to+point+radio+link+[microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning))) Links or Mobile Systems in mmWave bands.
4. UniMacro Model (400MHz – 3GHz) is the CE’s proprietary combination model developed over the years of practical experience with the operational planning
of cellular mobile networks in the frequency ranges from 400-2600 [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit). It had been fine tuned to produce coverage predictions that are most closely aligned
with what could be expected to be experienced by the actual mobile network users in the field. The model will model different path losses depending on radio
visibility conditions as follows:
a. Receive antenna in LOS condition – path loss modelled based on FSL principle;
b. Receive antenna in OLOS condition – path loss modelled using Extended Hata (Open Area) model with additional clutter loss calculated based on
Recommendation ITU-R P.2108 (ref URL);
c. Receive antenna in NLOS condition – path loss modelled using Extended Hata model with additional losses due to diffraction calculated based on
Recommendation ITU-R P.526 (ref URL) as well as clutter losses based on Rec. ITU-R P.2108 (ref URL).
5. ITU-R P.368 (10kHz – 30MHz)

---

Prediction Models. Default

---

CEC ITU-R (30MHz – 6GHz)
- For frequencies from about 30 [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit)
to about 6 GHz.
- Modelling:
- LOS
- OLOS
- NLOS
Diffraction Free Space Loss
Diffraction
H
obstacles
H
Clutter losses clutter [DSM](https://www.google.com/search?q=DSM+Digital+Surface+Model)
UE
[DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model)

---

Input Data
- [Elevation](https://www.google.com/search?q=elevation+model+[terrain](https://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography)+height+datum)
- Clutter classes* Geographic data
- Clutter height grid*
- Receiver settings
Network data
- Prediction model settings
Algorithm
* Optional

---

Path loss equation
Path loss in dB:
Offset coefficient (K ) - Constant offset ([dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit)). Default value 32
Off
Distance coefficient (K ) - Distance influence coefficient. Default value 20
LogD
Frequency coefficient (K ) - Frequency influence coefficient. Default value 20
LogF
L = k
o f f
+ k
l o g D
 l o g ( d ) + k
l o g F
 l o g ( f )

---

Path loss equation
Path loss in dB:
Offset coefficient (K ) - Constant offset ([dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit)). Default value 32
Off
Distance coefficient obstructed (K ) - Distance influence coefficient. Default value 30
LogD
Frequency coefficient (K ) - Frequency influence coefficient. Default value 20
LogF
L = k
o f f
+ k
l o g D
 l o g ( d ) + k
l o g F
 l o g ( f )

---

Clutter
- Diffraction loss for solid obstacle:
- Building clutter class
- [Elevation](https://www.google.com/search?q=elevation+model+[terrain](https://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography)+height+datum)
- Clutter loss
- Based on diffraction calculation
- P.2108 Clutter Loss
- Penetration loss (Outdoor – Indoor)
- Receiver loss

---

SKE Diffraction
Rec. ITU-R P.526
Idealized model of diffraction over a single obstruction.

d d
1 h > 0 2
 
1 2

---

Clutter LOS
P.2108 Clutter Loss Estimation
- Method 1: Additional clutter shadowing
loss with diffraction as dominant effect
(section 3.1)

---

Penetration loss (Outdoor – Indoor)
CE Outdoor to Indoor Path Loss calculation is realised based on method
recommended in 3GPP TR 38.901 (ref URL). This method accounts for
indoor portion of the total radio [signal propagation](https://www.google.com/search?q=signal+propagation+radio+wave) path as shown in picture:
Definition of indoor propagation path in 3GPP TR 38.901
For general purpose modelling of typical building entry losses, two types of loss profiles are assumed:
- Low-loss BEL Model assumes a wall penetration losses characteristic of average traditional
buildings;
- High-loss BEL Model assumes a wall penetration losses characteristic of modern thermally
insulated buildings.
The corresponding BEL and building penetration losses are calculated as follows:
Where:
L =2+0.2f L =5+4f L =23+0.3f f–frequencyinGHz.
glass concrete IIRglass

---

Prediction model manager
- Cellular Expert tab > Prediction Model
Manager
- Default can not be deleted and it takes
parameters from it for new models

---

LOS ITU-R P.542 (6GHz – 50GHz)
- For frequencies from about 6 GHz to about 100 GHz
Diffraction Free Space Loss
Diffraction
H
obstacles
H
Clutter losses clutter [DSM](https://www.google.com/search?q=DSM+Digital+Surface+Model+buildings+trees)
UE
[DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation+data)

---

Input Data
- Elevation
- Clutter classes* Geographic data
- Clutter height grid*
- Receiver settings
Network data
- Prediction model settings
Algorithm
* Optional

---

Path loss equation
Path loss in dB:
Offset coefficient (K ) - Constant offset (dBm). Default value 32
Off
Distance coefficient (K ) - Distance influence coefficient. Default value 20
LogD
Frequency coefficient (K ) - Frequency influence coefficient. Default value 20
LogF
L = k
o f f
+ k
l o g D
 l o g ( d ) + k
l o g F
 l o g ( f )

---

Clutter
- Diffraction loss
- Building clutter class
- Elevation
- Penetration loss (Outdoor – Indoor)

---

Single Knife Edge Diffraction
Rec. ITU-R P.526
Idealized model of diffraction over a single obstruction.

d d
1 h > 0 2
 
1 2

---

Penetration loss (Outdoor – Indoor)
CE Outdoor to Indoor Path Loss calculation is realised based on method
recommended in 3GPP TR 38.901 (ref URL). This method accounts for
indoor portion of the total radio [signal propagation](https://www.google.com/search?q=signal+propagation+radio+wave) path as shown in picture:
Definition of indoor propagation path in 3GPP TR 38.901
For general purpose modelling of typical building entry losses, two types of loss profiles are assumed:
- Low-loss BEL Model assumes a wall penetration losses characteristic of average traditional
buildings;
- High-loss BEL Model assumes a wall penetration losses characteristic of modern thermally
insulated buildings.
The corresponding BEL and building penetration losses are calculated as follows:
Where:
L =2+0.2f L =5+4f L =23+0.3f f–frequencyinGHz.
glass concrete IIRglass

---

LOS ITU-R P.525 (6GHz – 100GHz)
- For frequencies from about 6 GHz to about 100 GHz
Diffraction Free Space Loss
Diffraction
H
obstacles
H
Clutter losses clutter [DSM](https://www.google.com/search?q=DSM+Digital+Surface+Model+buildings+trees)
UE
[DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation+data)

---

Input Data
- Elevation
- Clutter classes* Geographic data
- Clutter height grid*
- Receiver settings
Network data
- Prediction model settings
Algorithm
* Optional

---

Path loss equation
Path loss in dB:
Offset coefficient (K ) - Constant offset (dBm). Default value 32
Off
Distance coefficient (K ) - Distance influence coefficient. Default value 20
LogD
Frequency coefficient (K ) - Frequency influence coefficient. Default value 20
LogF
L = k
o f f
+ k
l o g D
 l o g ( d ) + k
l o g F
 l o g ( f )

---

UniMacro
- Frequency: ~ 100 MHz - 2 GHz (3 GHz)
- Distance: up to 100 km
- 9999 Model ([Ericsson](https://www.google.com/search?q=Ericsson+telecom+network+vendor))
Diffraction Free Space Loss
Diffraction
H
obstacles
H
Clutter losses clutter DSM
UE
DTM

---

Input Data
- Elevation
- Clutter classes* Geographic data
- Clutter height grid*
- Receiver settings
Network data
- Prediction model settings
Algorithm
* Optional

---

Equation
- [Line-Of-Sight](https://www.google.com/search?q=line+of+sight+LOS+radio+link) Model Loss
- 9999 [Ericsson](https://www.google.com/search?q=Ericsson+telecom+network+vendor)
- Single Knife Edge Diffraction

---

Path Loss Equation: 9999 Ericsson
L = a + a log(d) + a log(h ) + a log(h )log(d)
Path loss in dB: H 0 1 2 B 3 B
( ( ))2
+ 3.2 log 11.75h + g( f )
M
g( f ) = 44.49log( f ) + 4.78(log( f ))
Default
Parameter Description
Value
a Constant offset in dB. This value is simply added to loss grid. By adjusting
this value, the mean error can be minimized. It regulates the absolute level of
36.8
the loss curve.
a Distance influence coefficient. Physically it represents loss dependant on
distance such as atmospheric (dust, hydrometeors, etc...) losses. It regulates
30.2
slope of the curve.
a Transmitter height influence coefficient. It is related to errors in DTM, real
Earth curvature, etc. It regulates loss curve vertical position like the a0, but -12.0
with respect to antenna height
a [Okumura-Hata](https://www.google.com/search?q=Okumura+Hata+propagation+model) type of multiplying factor for log(h )log(d) 0.1
3 B

---

9999 Ericsson: A0
- 9999 Model is very convenient for calibration
- Empirical parameters a0-a3 can be deduced from the measured path
loss dependence on distance – drive-tests
- a0 is a constant offset of path loss curve
P a t h L o
d
s
B
s
m
,
D i s
t a
n c e , k m
1 0 0
A
A
A
=
=
=
.
.
.

---

9999 Ericsson: A1
- 9999 Model is very convenient for calibration
- a1 regulates slope of the path loss curve
P a th L o
d
s
B
s
m
,
D is
ta
n c e , k m
1 0 0
A
A
A
=
=
=
.7
.7
.7

---

9999 Ericsson: A2
- 9999 Model is very convenient for calibration
- a2 regulates loss curve vertical position like a0, but with respect to
antenna height
P a th L o
d
s
B
s
m
,
D is
1 0
ta n c e , k m
1 0 0
A
A
A
A
A
=
=
=
=
=
-
-
-
-
-
h
h
h
h
h
=
=
=
=
=
m
m
m
m
m

---

9999 Ericsson: A3
- 9999 Model is very convenient for calibration
- a3 defines slope of the path loss curve for different [base station](https://www.google.com/search?q=base+station+[BTS](https://www.google.com/search?q=BTS+Base+Transceiver+Station+GSM+[2G](https://www.google.com/search?q=2G+GSM+mobile+network+second+generation))+[NodeB](https://www.google.com/search?q=NodeB+[3G](https://www.google.com/search?q=3G+UMTS+HSPA+mobile+network)+[UMTS](https://www.google.com/search?q=UMTS+[3G](https://www.google.com/search?q=3G+UMTS+HSPA+mobile+network)+Universal+Mobile+Telecommunications)+base+station)+[eNodeB](https://www.google.com/search?q=eNodeB+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+[4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)+mobile)+[4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)+base+station)+[gNodeB](https://www.google.com/search?q=gNodeB+[5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network)+NR+base+station))
antenna heights
Path Loss,
A3 = -0.5
dBm 170
A3 = 0.1
A3 = 0.6
1 10 100
Distance, km

---

Path loss equation
Path loss in dB:
K - Constant offset (dBm). Default value 32 (!)
Off
K - Distance influence coefficient. Default value 20
LogD
K - Frequency influence coefficient. Default value 20
LogF
L = k
o f f
+ k
l o g D
 l o g ( d ) + k
l o g F
 l o g ( f )

---

Clutter
- Diffraction loss for solid obstacle:
- Building clutter class
- Elevation
- Clutter loss
- Based on diffraction calculation
- P.2108 Clutter Loss
- Penetration loss (Outdoor – Indoor)
- Receiver loss

---

SKE Diffraction
Rec. ITU-R P.526
Idealized model of diffraction over a single obstruction.

d d
1 h > 0 2
 
1 2

---

Clutter LOS
P.2108 Clutter Loss Estimation
- Method 1: Additional clutter shadowing
loss with diffraction as dominant effect
(section 3.1)

---

Penetration loss (Outdoor – Indoor)
CE Outdoor to Indoor Path Loss calculation is realised based on method
recommended in 3GPP TR 38.901 (ref URL). This method accounts for
indoor portion of the total radio signal propagation path as shown in picture:
Definition of indoor propagation path in 3GPP TR 38.901
For general purpose modelling of typical building entry losses, two types of loss profiles are assumed:
- Low-loss BEL Model assumes a wall penetration losses characteristic of average traditional
buildings;
- High-loss BEL Model assumes a wall penetration losses characteristic of modern thermally
insulated buildings.
The corresponding BEL and building penetration losses are calculated as follows:
Where:
L =2+0.2f L =5+4f L =23+0.3f f–frequencyinGHz.
glass concrete IIRglass

---

Exercise
Description: C:\CE_Course\0. Descriptions
Name: 5. Prediction models.pdf

---

Thank you!
Tel.: +370 5 2150575
Email: info@cellular-expert.com
S.Konarskio g. 28A LT-03127 Vilnius
Lithuania
www.cellular-expert.com

---
