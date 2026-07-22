# 3.1.31 Audibility

Click this button to open Audibility tool.

![Image p189](../../../assets/images/ce-express/user-guide-v73/p189-img1.png)

![Image p189](../../../assets/images/ce-express/user-guide-v73/p189-img2.png)

| Parameter | Description |
|---|---|
| Calculation name | Name of the calculation that will be displayed in Prediction history. |
| Resolution | Prediction raster cell size in meters. |
| Siren Template | Option to use the parameters from the template if the siren misses the required parameters. |
Results:
- Audibility, dB. The siren sound prediction tool calculates the sound pressure level (SPL) at various
locations around a siren using ISO 9613-2 as the standard for sound propagation. The results are
represented in decibels (dB), showing how loud the siren is at different distances and conditions. Each

![Image p190](../../../assets/images/ce-express/user-guide-v73/p190-img1.png)
location's sound pressure level is affected by several factors:
1. Distance from the Source (Siren)
o SPL decreases as the distance from the siren increases due to geometrical spreading.
o The tool provides results that help visualize how sound intensity reduces at different
locations.
2. Obstacles and Terrain
o Buildings, hills, and other obstacles can block or reflect sound, reducing the SPL.
o Flat, open areas will have a higher SPL compared to urban environments with multiple
obstacles.
3. Atmospheric Conditions
o Atmospheric factors like temperature, humidity, and wind influence sound propagation.
o These effects are taken into account according to ISO 9613-2.
4. Frequency-Dependent Attenuation
o Higher frequencies (treble) attenuate faster than lower frequencies (bass).
o The tool might calculate the overall SPL or provide frequency-specific results.
- The best server raster shows the identification of siren generating the strongest sound value at
each pixel.
