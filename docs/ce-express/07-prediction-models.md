---
id: ce-express-prediction-models
title: Prediction Models
product: CE Express
version: "7.3"
category: Calculations
order: 7
related:
  - ce-express-rf-prediction
  - ce-express-model-tuning
  - geodata-requirements
---

# Prediction Models

Prediction models define how **[signal propagation]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=signal+propagation+radio+wave) losses** are calculated across the coverage area.

## How CE Evaluates Propagation

Instead of applying a single formula everywhere, [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) evaluates the **radio visibility condition** between each transmitter and each receiver [pixel](https://www.google.com/search?q=pixel+raster+grid+[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+resolution), then applies the most appropriate loss model:

| Visibility Condition | Abbreviation | Description |
|---------------------|--------------|-------------|
| [Line-of-Sight]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=line+of+sight+[LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation)+radio+link) | [LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation) | Clear unobstructed path |
| [Near Line-of-Sight](https://www.google.com/search?q=Near+Line+of+Sight+NLOS1+radio+propagation) | NLOS1 | Marginally obstructed ([Fresnel zone](https://www.google.com/search?q=Fresnel+zone+radio+link+clearance) partially blocked) |
| Non-[Line-of-Sight](https://www.google.com/search?q=line+of+sight+LOS+radio+link) | [NLOS](https://www.google.com/search?q=NLOS+Non+Line+of+Sight+radio+propagation) | Fully obstructed path |

Radio visibility is evaluated using: [DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation) ([terrain](https://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography)), Obstacles, and [Clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) path profiles.

This approach enables **near-deterministic modeling** — [terrain](https://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography), obstacles, and [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) are explicitly considered for every calculation [pixel](https://www.google.com/search?q=pixel+raster+grid+[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+resolution).

## Available Models

### __S4__

- **Type:** Empirical
- **Frequency range:** 150 – 1500 [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit)
- **Environments:** Urban, Suburban, Rural, Open
- **Use case:** Macro cells, large coverage areas, legacy [2G](https://www.google.com/search?q=2G+GSM+mobile+network+second+generation)/[3G](https://www.google.com/search?q=3G+UMTS+HSPA+mobile+network) networks
- **Data needed:** [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain) + [Clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) (optional)

### __S6__

- **Type:** Empirical (extension of [Okumura-Hata](https://www.google.com/search?q=Okumura+Hata+propagation+model))
- **Frequency range:** Up to 2 [GHz](https://www.google.com/search?q=GHz+gigahertz+frequency+unit)
- **Environments:** Urban, Suburban
- **Use case:** [3G](https://www.google.com/search?q=3G+UMTS+HSPA+mobile+network)/[UMTS](https://www.google.com/search?q=UMTS+3G+mobile+network) macro planning
- **Data needed:** [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain) + Clutter

### __S10__

- **Type:** Semi-empirical (considers building geometry)
- **Frequency range:** 800 [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit) – 2 [GHz](https://www.google.com/search?q=GHz+gigahertz+frequency+unit)
- **Environments:** Urban micro cells
- **Use case:** Dense urban environments, small cells
- **Data needed:** [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster) + Clutter + Building data (heights)

### __S11__ (Standard Propagation Model)

- **Type:** Configurable empirical
- **Frequency range:** Wide (depends on configuration)
- **Use case:** General-purpose; can be calibrated to local conditions
- **Data needed:** [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster) + Clutter
- **Key feature:** Adjustable coefficients (K1–K6) for local tuning

### __S12__ (3D)

- **Type:** Physics-based (deterministic)
- **Accuracy:** Highest
- **Use case:** Urban micro planning, indoor-to-outdoor, small cells
- **Data needed:** DEM + Clutter + **Full [3D building](https://www.google.com/search?q=3D+building+model+urban+GIS) models required**
- **Speed:** Slowest — recommended for small areas only

### CE Custom Models

- [Site](https://www.google.com/search?q=cell+site+tower+base+station+location)-specific models tuned for particular deployment environments
- Created using [Model Tuning](#ce-express-model-tuning) against drive-test measurements

## Selecting a Model

In the Prediction Models tool, configure the model:

1. Choose the **model type**
2. Set the **environment** (Dense Urban / Urban / Suburban / Rural / Open)
3. Configure **LOS, NLOS1, [NLOS](https://www.google.com/search?q=NLOS+Non+Line+of+Sight+radio+propagation)** model assignments (can use different models per visibility condition)
4. Adjust **model coefficients** if required (advanced)

Models can be set:
- **Per [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase)** — applies to all cells unless overridden
- **Per cell** — override [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase) default for specific cells

## Model Tuning / Calibration

Improve prediction accuracy by calibrating against real measurements:

1. [Import](https://www.google.com/search?q=data+import+GIS+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) drive-test data ([CSV](https://www.google.com/search?q=CSV+comma-separated+values+file+format) with Lat/Lon/Signal level/Cell ID)
2. [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) → **[Model Tuning](https://www.google.com/search?q=propagation+model+tuning+calibration+drive+test)** tool
3. The wizard compares predicted vs. measured values
4. Adjusts model coefficients to minimize mean error
5. Save the tuned model for future predictions

→ See [Model Tuning →](#ce-express-model-tuning)

## Choosing the Right Model

| Environment | Recommended Model |
|-------------|------------------|
| Rural / Open terrain | [Okumura-Hata](https://www.google.com/search?q=Okumura+Hata+propagation+model+radio+frequency) (Rural/Open) |
| Suburban | [COST-231 Hata](https://www.google.com/search?q=COST+231+Hata+propagation+model) or [Okumura-Hata](https://www.google.com/search?q=Okumura+Hata+propagation+model+radio+frequency) (Suburban) |
| Urban macro | [COST-231](https://www.google.com/search?q=COST+231+propagation+model+telecom) Hata (Urban) |
| Dense urban, small cells | [COST-231 Walfisch-Ikegami](https://www.google.com/search?q=COST+231+Walfisch+Ikegami+urban+model) or [Ray Tracing](https://www.google.com/search?q=ray+tracing+radio+propagation+3D) |
| [5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network) (sub-6 GHz) | [SPM](https://www.google.com/search?q=SPM+Standard+Propagation+Model+radio) or tuned [COST-231](https://www.google.com/search?q=COST+231+propagation+model+telecom) |
| [Backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network) / [Point-to-point](https://www.google.com/search?q=point+to+point+radio+link+[microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning)) | See [Radio Link Prediction](#ce-express-radio-link) |

## Related Topics

- [RF Prediction →](#ce-express-rf-prediction)
- [Model Tuning →](#ce-express-model-tuning)
- [Geodata Requirements →](#geodata-requirements)
