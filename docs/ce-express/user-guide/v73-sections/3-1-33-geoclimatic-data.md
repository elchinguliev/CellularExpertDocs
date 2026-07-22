# 3.1.33 Geoclimatic data

Click this button to open Geoclimatic data tool.
Geoclimatic Data is a tool that lets you adjust the geoclimatic settings that will be used in certain calculations

![Image p191](../../../assets/images/ce-express/user-guide-v73/p191-img1.png)

![Image p191](../../../assets/images/ce-express/user-guide-v73/p191-img2.png)

![Image p191](../../../assets/images/ce-express/user-guide-v73/p191-img3.png)
(e.g. Link Prediction).

3.1.33.1 Gaseous Absorption
Gaseous absorption define values for dry air pressure and water vapour density. These values can be
obtained from predefined geoclimatic data maps. Water vapour density data according to ITU-R P.836-3.
It is used in gaseous absorption evaluation.
Dry Air Pressure
The atmospheric pressure contributed by air that contains no water vapor, typically measured in
hectopascals (hPa).
Water Vapour Density
The mass of water vapor present in a unit volume of air, typically measured in grams per cubic meter (g/m³).

![Image p192](../../../assets/images/ce-express/user-guide-v73/p192-img1.png)

![Image p192](../../../assets/images/ce-express/user-guide-v73/p192-img2.png)

Use Geoclimatic Data
Enable/Disable this Geoclimatic data
Water Vapour Density Data
A dropdown menu that allows the user to select the source or type of data used to determine water vapor
density.
3.1.33.2 Temperature
Annual mean surface temperature at 2m above the surface of the Earth according to ITU-R P.1510. The
data is used to evaluate the thermal noise of a receiver.
Annual Temperature
Annual Temperature expressed in Kelvins.
Use Geoclimatic Data
Enable/Disable this Geoclimatic data
Annual Temperature Data
A dropdown menu allowing the user to select the dataset from which the annual temperature data should
be sourced.
3.1.33.3 Multipath Fading
The Multipath Fading page defines refractivity data and calculation parameters for ITU and Vigants-Barnett
methods.
Worst month-to-annual statistics conversion can be performed according to ITU-R P. 530 or ITU-R P. 841
methods.
Refractivity gradient data is based on ITU-R P.453-9. Refractivity gradient data is used for multipath fading

![Image p193](../../../assets/images/ce-express/user-guide-v73/p193-img1.png)
analysis.

ITU Method
Enable/Disable the ITU Method
ITU-R P.530 version
A dropdown menu allowing the user to select the ITU-R P.530 version.

![Image p194](../../../assets/images/ce-express/user-guide-v73/p194-img1.png)

Use Geoclimatic Data
Enable/Disable this Geoclimatic data.
Geoclimatic Factor (Define value manually)
A field to input or calculate a factor used in propagation modeling, affecting the prediction of multipath
fading.
Geoclimactic Factor (Calculate)
Calculate the geoclimactic factor used in propagation modeling, affecting the prediction of multipath fading.
- Approximation of terrain roughness - Options to select how terrain roughness is modeled in the
calculations - as a constant value or as a linear approximation.
- Percentage of time that refractivity gradient in the lowest 100 m is less than 100 units/km -
An input field for the percentage of time when the refractivity gradient at low altitudes meets a
specific threshold.
- Co, dB / Lat, dB / Lon, dB - Fields to input correction values in decibels for specific geographic
coordinates, possibly related to the orientation or position of the transmitter/receiver.
| Parameter | Description |
|---|---|
| Percentage of Time / Design | A dropdown menus to choose the granularity of the time percentage for which the calculations are relevant, and the level of detail required for planning. |
| Use Viggants-Barnett Method | Enabled/Disabled Viggants-Barnett Method. |
| Worst month conversion | A section to select the ITU recommendation (either ITU-R P.530 or ITU-R P.841) for converting worst- month statistics to annual statistics. |
Interf. correction factor for multipath and focusing effects
Input for the percentage of time to apply an interference correction factor to account for multipath and
focusing effects.
3.1.33.4 Rain Fading
The rain fading page defines rain regions (ITU and Crane) for rain rate statistics and calculation methods
(ITU and Crane). The rain rate exceedance parameter for 0.01% of the time can be set manually or
automatically according to the rain zone.

| Parameter | Description |
|---|---|
| Geoclimatic data - ESA rain rate data / ESA rain rate | Options to select the dataset (such as "ESARAIN_V5") and the specific field within that dataset (like "MT") for rain rate data, used for calculating rain attenuation. |
| Fading method - ITU method / ITU-R P.530 version | A checkbox to select the ITU method for rain fading calculations and a dropdown to choose the version of the ITU-R P.530 recommendation being applied. |
| Crane | This is a model selection option related to the Crane model for calculating rain attenuation. |
End-to-end reliability method - Multi-hop / Two-way
Selection options for the method of calculating the reliability of a signal in a communication path that may

![Image p196](../../../assets/images/ce-express/user-guide-v73/p196-img1.png)
involve multiple hops or two-way transmission.
3.1.33.5 Statistics
These settings are used to handle statistical conversions for telecommunication planning, ensuring that
systems are designed to cope with the worst-case scenarios based on historical data and predictive models.

Define
Options to either define a fixed conversion factor or to calculate it based on additional inputs.
Q1 (1...12)
An input field likely used to define a conversion factor or another parameter for a specific month or set of
months.
Beta
An input field for the beta parameter, which may be part of the statistical model or conversion formula within

![Image p197](../../../assets/images/ce-express/user-guide-v73/p197-img1.png)

![Image p197](../../../assets/images/ce-express/user-guide-v73/p197-img2.png)
the ITU-R P.841 recommendation.
