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

Prediction models define how **[signal propagation](https+TLS+secure+protocol)://www.google.com/search?q=signal+propagation+radio+wave) losses** are calculated across the coverage area.

## How CE Evaluates Propagation

Instead of applying a single formula everywhere, [CE Express](#ce-express-overview) evaluates the **radio visibility condition** between each transmitter and each receiver pixel+resolution), then applies the most appropriate loss model:

| Visibility Condition | Abbreviation | Description |
|---------------------|--------------|-------------|
| [Line-of-Sight](https+TLS+secure+protocol)://www.google.com/search?q=line+of+sight+LOS+radio+link) | LOS | Clear unobstructed path |
| Near Line-of-Sight | NLOS1 | Marginally obstructed ([Fresnel zone](#ce-express-profile) partially blocked) |
| Non-Line-of-Sight | NLOS | Fully obstructed path |

Radio visibility is evaluated using: [DTM](#geodata-dem) (terrain+topography)), Obstacles, and [Clutter](#kw:clutter-classes-grid:geodata-clutter) path profiles.

This approach enables **near-deterministic modeling** — terrain+topography), obstacles, and [clutter](#kw:clutter-classes-grid:geodata-clutter) are explicitly considered for every calculation pixel+resolution).

## Available Models

### __S4__

- **Type:** Empirical
- **Frequency range:** 150 – 1500 MHz
- **Environments:** Urban, Suburban, Rural, Open
- **Use case:** Macro cells, large coverage areas, legacy 2G/3G networks
- **Data needed:** [DEM](#geodata-dem) + Clutter (optional)

### __S6__

- **Type:** Empirical (extension of [Okumura-Hata](#ce-express-prediction-models))
- **Frequency range:** Up to 2 GHz
- **Environments:** Urban, Suburban
- **Use case:** 3G/UMTS macro planning
- **Data needed:** [DEM](#geodata-dem) + Clutter

### __S10__

- **Type:** Semi-empirical (considers building geometry)
- **Frequency range:** 800 MHz – 2 GHz
- **Environments:** Urban micro cells
- **Use case:** Dense urban environments, small cells
- **Data needed:** DEM + Clutter + Building data (heights)

### __S11__ (Standard Propagation Model)

- **Type:** Configurable empirical
- **Frequency range:** Wide (depends on configuration)
- **Use case:** General-purpose; can be calibrated to local conditions
- **Data needed:** DEM + Clutter
- **Key feature:** Adjustable coefficients (K1–K6) for local tuning

### __S12__ (3D)

- **Type:** Physics-based (deterministic)
- **Accuracy:** Highest
- **Use case:** Urban micro planning, indoor-to-outdoor, small cells
- **Data needed:** DEM + Clutter + **Full 3D building models required**
- **Speed:** Slowest — recommended for small areas only

### CE Custom Models

- Site-specific models tuned for particular deployment environments
- Created using [Model Tuning](#ce-express-model-tuning) against drive-test measurements

## Selecting a Model

In the Prediction Models tool, configure the model:

1. Choose the **model type**
2. Set the **environment** (Dense Urban / Urban / Suburban / Rural / Open)
3. Configure **LOS, NLOS1, NLOS** model assignments (can use different models per visibility condition)
4. Adjust **model coefficients** if required (advanced)

Models can be set:
- **Per [workspace](#kw:creating-a-workspace:ce-express-workspace)+[workspace](#kw:creating-a-workspace:ce-express-workspace)+project+geodatabase)** — applies to all cells unless overridden
- **Per cell** — override workspace+workspace+project+geodatabase) default for specific cells

## Model Tuning / Calibration

Improve prediction accuracy by calibrating against real measurements:

1. Import) drive-test data (CSV with Lat/Lon/Signal level/Cell ID)
2. [CE Express](#ce-express-overview) → **[Model Tuning](#kw:model-tuning-calibration:ce-express-prediction-models)** tool
3. The wizard compares predicted vs. measured values
4. Adjusts model coefficients to minimize mean error
5. Save the tuned model for future predictions

→ See [Model Tuning →](#ce-express-model-tuning)

## Choosing the Right Model

| Environment | Recommended Model |
|-------------|------------------|
| Rural / Open terrain | [Okumura-Hata](#ce-express-prediction-models) (Rural/Open) |
| Suburban | [COST-231 Hata](#ce-express-prediction-models) or Okumura-Hata (Suburban) |
| Urban macro | [COST-231 Hata](#ce-express-prediction-models) (Urban) |
| Dense urban, small cells | [COST-231 Walfisch-Ikegami](#ce-express-prediction-models) or [Ray Tracing](#ce-express-prediction-models) |
| 5G (sub-6 GHz) | [SPM](#ce-express-prediction-models) or tuned [COST-231](#ce-express-prediction-models) |
| Backhaul / Point-to-point+radio+link+planning)) | See [Radio Link Prediction](#ce-express-radio-link) |

## Related Topics

- [RF Prediction →](#ce-express-rf-prediction)
- [Model Tuning →](#ce-express-model-tuning)
- [Geodata Requirements →](#geodata-requirements)
