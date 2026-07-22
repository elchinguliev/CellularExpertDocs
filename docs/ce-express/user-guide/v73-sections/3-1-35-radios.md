# 3.1.35 Radios

Click this button ![icon](../../../assets/images/ce-express/user-guide-v73/p201-img2.png) to open Radios tool.
The tool enables you to create and preview radios that will be necessary to create a link and later be used

![Image p201](../../../assets/images/ce-express/user-guide-v73/p201-img1.png)
in calculations.

Move the mouse cursor over the radio and delete radio using Delete button.
By clicking an already existing radio, you can edit its properties and save them.

![Image p202](../../../assets/images/ce-express/user-guide-v73/p202-img1.png)

![Image p202](../../../assets/images/ce-express/user-guide-v73/p202-img2.png)

3.1.35.1 Add new radio
To create a radio press the New radio button.

![Image p203](../../../assets/images/ce-express/user-guide-v73/p203-img1.png)

General
Model
Radio identification or name.
Manufacturer
Radio manufacturer (company or entity).
Bandwidth, MHz
Range of frequencies within which the radio operates, value in MHz.
MTBF, h
Mean time between failures: average time (in hours) between successive failures of the radio system during

![Image p204](../../../assets/images/ce-express/user-guide-v73/p204-img1.png)
normal operation, indicating reliability.
MTTR, h
Mean time to repair: average time (in hours) required to repair the radio system after a failure occurs,
indicating maintainability.
Dispersive Fade Margin, dB
Additional signal strength required to overcome dispersion and fading effects in the radio communication
system, measured in dB.
Emission Designator
Code describing the characteristics of the radio emission, including modulation type, signal nature, and
bandwidth.

Receiver
BER 10-3 Threshold, dBm
Receiver sensitivity threshold for BER = 10-6.
BER 10-6 Threshold, dBm
Receiver sensitivity threshold for BER = 10-3.
Noise Floor, dB
Refers to the minimum power level of unwanted noise or interference at the receiver at the base station.
Noise Figure, dB
Measure of the degradation of the signal-to-noise ratio (SNR) as a signal passes through a radio component

![Image p205](../../../assets/images/ce-express/user-guide-v73/p205-img1.png)
or system. Value in dB. Required for 4G and 5G technologies.
Receiver Noise, dBm
The sum of Noise Floor and Noise Figure.
Residual BER
The remaining bit error rate after all error correction methods have been applied.
XPIF, dB

Cross-polarization interference factor: interference caused by signal components with orthogonal
polarization states, indicating the impact of cross-polarization on system performance, expressed in
decibels (dB). The default value is 20. The value should be higher than 0 for rain ITU fading calculations to
work.
Manufacturer’s guaranteed minimum XPD, dB
The manufacturer’s guaranteed minimum cross-polar discrimination, expressed in decibels (dB). The
default value is 30.
Carrier-to-interference ratio for a reference BER, dB
Carrier-to-interference ratio for a reference bit error rate, expressed in decibels (dB). The default value is

![Image p206](../../../assets/images/ce-express/user-guide-v73/p206-img1.png)

![Image p206](../../../assets/images/ce-express/user-guide-v73/p206-img2.png)
35.
Transmitter
Power, dBm
Power value in dBm.
Automatic Transfer Power Control Range (ATPC), dB
The range over which the radio can automatically adjust its transmission power, measured in dB.

The modulations are used in MW link calculations and specifically can be defined for Radios.
Modulations
Add modulation
A new modulation with default values can be initialized.
