---
id: training-rf-prediction
title: "Training 04: RF Prediction and Scenario Analysis"
product: CE Express
category: Training
order: 4
related:
  - ce-express-rf-prediction
  - ce-express-quick-rf
  - ce-express-prediction-models
  - ce-express-prediction-history
---

# Training Module 04 — RF Prediction and Scenario Analysis

**Duration:** ~2 hours | **Level:** Intermediate

## Objectives

By the end of this module, you will be able to:

- Run **Quick RF Predictions** for what-if testing
- Run **full RF Predictions** for one or multiple cells
- Understand how geodata influences prediction calculations
- Visualize and customize prediction results
- Compare multiple prediction outputs
- Use Networks for batch predictions

## Key Concepts

### What Is an RF Prediction?

An [RF prediction](https://www.google.com/search?q=RF+radio+frequency+prediction+coverage) produces **map-based [raster]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=raster+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+grid+data+format) outputs** representing expected signal or performance. These are influenced by:

- [Network objects]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=radio+network+objects+sites+cells+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)) (cells, sites, antennas — [azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north), tilt, height, power, frequency)
- Geodata ([terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) [elevation](https://www.google.com/search?q=elevation+model+[terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography)+height+datum), [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio)/[land use](https://www.google.com/search?q=land+use+land+cover+classification+GIS), obstacles)
- Equipment definitions (antenna patterns, [propagation models](https://www.google.com/search?q=radio+propagation+models+comparison+telecom), calculation templates)

**→ Full documentation: [RF Prediction →](#ce-express-rf-prediction)**

### Quick Prediction vs Full RF Prediction

| Feature | Quick RF | Full RF |
|---------|----------|---------|
| Speed | Instant | Standard |
| [DB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit) impact | No changes to database | Saves to prediction history |
| Use case | What-if, parameter comparison | Final results, reporting |

## Exercise 1 — Quick RF Prediction

1. Select a [cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) on the map (single click)
2. Click **[Quick RF Prediction](https://www.google.com/search?q=Quick+RF+Prediction+what+if+testing+CE+Express)** in the left toolbar
3. Change the [azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north) to 90° in the Quick RF panel
4. Click **Run** — result appears immediately on the map
5. Change azimuth to 180° → **Run** again
6. Compare the two results

**Observe:** The database has NOT been changed. This is for testing only.

## Exercise 2 — Full RF Prediction

1. Select 3 cells on the map (use Rectangle selection)
2. Click **[RF Prediction](https://www.google.com/search?q=RF+radio+frequency+prediction+coverage+planning)** in the left toolbar
3. Set parameters:
   - Prediction type: **Coverage (signal level)**
   - [Resolution](https://www.google.com/search?q=spatial+resolution+[raster](https://www.google.com/search?q=raster+GIS+grid+data+format)+GIS+accuracy): **50 m**
   - Radius: **15 km**
   - [Propagation model](https://www.google.com/search?q=radio+wave+propagation+model+telecom): **[COST-231 Hata](https://www.google.com/search?q=COST+231+Hata+propagation+model+urban)**
4. Click **Run**
5. Wait for the prediction to complete (watch the progress bar)
6. View results in the Prediction History panel

**→ Prediction models documentation: [Prediction Models →](#ce-express-prediction-models)**

## Exercise 3 — Best Server Prediction

1. Select all cells in an area (use Polygon selection)
2. [RF Prediction](https://www.google.com/search?q=RF+radio+frequency+prediction+coverage+planning) → Prediction type: **[Best Server](https://www.google.com/search?q=best+server+analysis+coverage+planning+RF)**
3. [Resolution](https://www.google.com/search?q=spatial+resolution+raster+GIS+accuracy): **50 m** | Radius: **20 km**
4. Click **Run**
5. Observe which [cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) "wins" each area

## Exercise 4 — Network-Based Prediction

1. Click **Networks** tool in the left toolbar
2. Click **New network**
3. Name: `Training_4G_Network`
4. Feature type: **Cells**
5. Filter by attribute: Technology = **[4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)**
6. Click **Save**
7. In the network item → click **Calculate**
8. All [4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology) cells are calculated automatically

**→ Networks documentation: [Networks Tool →](#ce-express-networks)**

## Exercise 5 — Comparing Predictions

1. Open **Prediction History**
2. Enable two different prediction results
3. Use the **opacity slider** to switch between them
4. Click **Compare** to view side-by-side statistics

## Exercise 6 — Exporting Results

1. In Prediction History → select a result layer
2. Click **[Export](https://www.google.com/search?q=data+export+GIS+raster+vector)** → save as [GeoTIFF](https://www.google.com/search?q=GeoTIFF+raster+geospatial+format)
3. The raster file can be used in other [GIS](https://www.google.com/search?q=GIS+Geographic+Information+System) software or shared with clients

## Related Documentation

- **RF Prediction:** [RF Prediction →](#ce-express-rf-prediction)
- **Quick RF:** [Quick RF Prediction →](#ce-express-quick-rf)
- **Prediction Models:** [Prediction Models →](#ce-express-prediction-models)
- **Troubleshooting:** [RF Prediction Troubleshooting →](#troubleshooting-rf-prediction)
