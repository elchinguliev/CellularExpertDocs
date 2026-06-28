---
id: ce-express-radio-link
title: Radio Link (Microwave) Prediction
product: CE Express
version: "7.3"
category: Calculations
order: 9
related:
  - ce-express-profile
  - ce-express-mw-equipment
  - ce-express-prediction-models
---

# Radio Link (Microwave) Prediction

[CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) includes a complete **[microwave]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=microwave+[backhaul]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning) (MW) [backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network) planning** module for [point-to-point](https://www.google.com/search?q=point+to+point+radio+link+[microwave](https://www.google.com/search?q=microwave+backhaul+radio+link+planning)) and point-to-multipoint radio links.

## Creating a Radio Link

1. Select two sites on the map
2. Right-click → **Create Link** (or use Features tool → Add Link)
3. Configure link parameters:

### Link Parameters

| Parameter | Description |
|-----------|-------------|
| **A-[site](https://www.google.com/search?q=cell+site+tower+base+station+location) / B-[site](https://www.google.com/search?q=cell+site+tower+base+station+location)** | Both ends of the link |
| **Frequency ([GHz](https://www.google.com/search?q=GHz+gigahertz+frequency+unit))** | Operating frequency |
| **[Polarisation](https://www.google.com/search?q=antenna+polarisation+horizontal+vertical)** | Horizontal (H) or Vertical (V) |
| **Channel [bandwidth](https://www.google.com/search?q=channel+bandwidth+radio+frequency+[MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit))** | [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit) |
| **Antenna (A-end / B-end)** | Parabolic antenna from library |
| **Radio model** | Modem/radio equipment from library |

## Link Budget Calculation

Click **Link Prediction** → **Calculation** to compute:

| Output | Description |
|--------|-------------|
| **Free-space [path loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit))** | [FSPL](https://www.google.com/search?q=FSPL+Free+Space+Path+Loss+calculation) = 20·log(d) + 20·log(f) + 32.44 ([dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit)) |
| **Atmospheric [absorption](https://www.google.com/search?q=atmospheric+absorption+radio+signal)** | Gas [absorption](https://www.google.com/search?q=atmospheric+absorption+radio+signal) (oxygen, water vapour) per [ITU-R P.676](https://www.google.com/search?q=ITU-R+P.676+atmospheric+attenuation) |
| **Received Signal Level (RSL)** | Signal strength at receiver ([dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit)) |
| **System gain** | Tx power + both antenna gains − losses |
| **[Fade margin](https://www.google.com/search?q=fade+margin+link+budget+microwave+dB)** | RSL minus receiver [sensitivity](https://www.google.com/search?q=receiver+sensitivity+[dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit)+radio) (dB) |

## Geoclimatic Data

[CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) uses [ITU-R](https://www.google.com/search?q=ITU+R+radio+communication+standard) P-series recommendations for fade calculations:

| Factor | [ITU-R](https://www.google.com/search?q=ITU+R+International+Telecommunication+Union+Radio) Reference | Description |
|--------|----------------|-------------|
| **[Gaseous absorption](https://www.google.com/search?q=gaseous+absorption+oxygen+water+vapour+radio)** | P.676 | Frequency-dependent gas [attenuation](https://www.google.com/search?q=signal+attenuation+loss+radio+propagation) |
| **Temperature** | P.453 | Affect refractivity and [multipath](https://www.google.com/search?q=multipath+propagation+fading+radio) |
| **[Multipath fading](https://www.google.com/search?q=[multipath](https://www.google.com/search?q=multipath+propagation+fading+radio)+fading+radio+propagation+effect)** | P.530 | Statistical fading due to atmospheric layering |
| **Rain fading** | P.838 | Rain-induced [attenuation](https://www.google.com/search?q=signal+attenuation+loss+radio+propagation) |
| **Statistics** | P.530 | Annual [availability](https://www.google.com/search?q=link+availability+percentage+microwave+ITU) % |

## Availability Calculation

The [link budget](https://www.google.com/search?q=link+budget+microwave+radio+calculation) includes [ITU-R](https://www.google.com/search?q=ITU+R+International+Telecommunication+Union+Radio) **[availability](https://www.google.com/search?q=link+availability+percentage+microwave+ITU) prediction**:

| Availability | Typical Use |
|-------------|------------|
| 99.999% | Critical infrastructure (telecom backhaul) |
| 99.99% | High-availability links |
| 99.9% | Standard commercial links |

## Reflections

The **Reflections** tab analyses signal reflections from [terrain](https://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography) and water bodies that can cause multipath [interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent) on the link.

## Link Prediction Report

Click **[Export](https://www.google.com/search?q=data+export+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+raster+vector)** → generates a PDF report with:
- Link parameters summary
- [Path profile](https://www.google.com/search?q=path+profile+[terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography)+microwave+link)
- [Link budget](https://www.google.com/search?q=link+budget+microwave+radio+calculation) table
- Availability calculation
- [Fade margin](https://www.google.com/search?q=fade+margin+link+budget+microwave+dB) analysis

## Multi-Hop Paths

For multi-hop backhaul:
1. Create links between consecutive sites
2. [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) calculates end-to-end performance for each hop
3. Total availability = product of individual hop availabilities

## MW Equipment Library

→ See [MW Equipment →](#ce-express-mw-equipment)

To use Link Prediction, assign antenna and radio models from the equipment library to each link endpoint.

## Automatic Frequency Planning (AFP)

For mesh and multi-link networks, use **[AFP](https://www.google.com/search?q=Automatic+Frequency+Planning+radio+network)** to automatically assign frequencies minimizing [interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent).

→ See [Automatic Frequency Planning →](#ce-express-afp)

## Related Topics

- [Profile / Line of Sight →](#ce-express-profile)
- [MW Equipment Library →](#ce-express-mw-equipment)
- [Mesh Networks →](#ce-express-mesh)
