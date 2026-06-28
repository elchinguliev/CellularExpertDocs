# RF Prediction

[RF Prediction]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=RF+radio+frequency+prediction+coverage+planning) calculates radio coverage for a set of cells across a defined area. The output is a set of [raster]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=raster+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+grid+data+format) layers — [RSRP](https://www.google.com/search?q=RSRP+Reference+Signal+Received+Power+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+4G)), [SINR](https://www.google.com/search?q=SINR+Signal+Interference+Noise+Ratio), [throughput](https://www.google.com/search?q=network+throughput+downlink+uplink+[capacity](https://www.google.com/search?q=network+capacity+planning+telecom)), and [best server](https://www.google.com/search?q=best+server+analysis+coverage+planning+RF) — that can be displayed on the map and published to [ArcGIS Portal](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+Portal+enterprise+web+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)).

## Prerequisites

Before running a prediction, make sure you have:

1. ✅ A **[workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase)** selected with a valid geodata folder path
2. ✅ `elevation.tif` in the geodata folder (Projected CRS, [NoData](https://www.google.com/search?q=NoData+raster+value+GIS+missing+data) = -9999)
3. ✅ At least one **[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)** with latitude, longitude, and cell_name defined
4. ✅ A **prediction model** configured for the target technology ([4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology) or [5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network))
5. ✅ (Recommended) **Antenna patterns** assigned to cells

> See [Geodata](geodata.md), [Network Objects](network-objects.md), and [Antenna Patterns](antenna-patterns.md) if any of these are not yet set up.

## Running a Full RF Prediction

### Step 1 — Select Cells

1. Open the **Features** tool (or use the Rectangle Selection tool on the map).
2. Select the cells you want to include in the prediction.
3. Click **Show in Table → Cells** to confirm your selection.

### Step 2 — Open RF Prediction

Click the **[RF Prediction](https://www.google.com/search?q=RF+radio+frequency+prediction+coverage+planning)** tool in the left toolbar.

### Step 3 — Configure Parameters

| Parameter | Description | Recommendation |
|---|---|---|
| **Technology** | [4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology) ([LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+4G+mobile)) or [5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network) (NR) | Match your [cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) technology |
| **[Resolution](https://www.google.com/search?q=spatial+resolution+[raster](https://www.google.com/search?q=raster+GIS+grid+data+format)+GIS+accuracy)** | [Pixel](https://www.google.com/search?q=pixel+raster+grid+cell+resolution) size in metres | 50–100 m for quick checks; 10–25 m for final results |
| **[Best server](https://www.google.com/search?q=best+server+analysis+coverage+planning+RF) count** | How many best servers to calculate per [pixel](https://www.google.com/search?q=pixel+raster+grid+cell+resolution) | Minimum 3; use 5 for [interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent) analysis |
| **Prediction model** | The propagation formula to use | Select the model configured for your area |

### Step 4 — Calculate

Click **Calculate**. The prediction job is submitted to the [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) server.

Monitor progress in **Prediction History** (panel at the bottom of the screen):
- 🟡 Yellow = calculating
- 🟢 Green = complete
- 🔴 Red = error

## Quick RF Prediction

Quick RF is a fast, single-cell field strength preview. Use it for a rapid sanity check without running a full job.

1. Open the **[Quick RF Prediction](https://www.google.com/search?q=Quick+RF+Prediction+what+if+testing+CE+Express)** tool.
2. Set **[Resolution](https://www.google.com/search?q=spatial+resolution+raster+GIS+accuracy)** to 1 for best quality.
3. Hold **CTRL** and click on a cell — the prediction runs instantly.
4. View results in **Layers → Prediction results**.

> Quick RF calculates field strength only. For [RSRP](https://www.google.com/search?q=RSRP+Reference+Signal+Received+Power+[LTE](https://www.google.com/search?q=LTE+Long+Term+Evolution+4G+mobile)+4G), [SINR](https://www.google.com/search?q=SINR+signal+interference+noise+ratio+LTE), [throughput](https://www.google.com/search?q=network+throughput+downlink+uplink+[capacity](https://www.google.com/search?q=network+capacity+planning+telecom)), and multi-cell best server analysis, use the full RF Prediction tool.

## Prediction Outputs

| Output Layer | Unit | Description |
|---|---|---|
| [RSRP](https://www.google.com/search?q=RSRP+Reference+Signal+Received+Power+LTE+4G) (1st–5th server) | [dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit) | Reference Signal Received Power per best server |
| Best Server ID (1st–5th) | Cell ID | Which cell is strongest at each point |
| RSSI | [dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit) | Total received power including [interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent) |
| [RSRQ](https://www.google.com/search?q=RSRQ+Reference+Signal+Received+Quality+LTE) | [dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit) | Signal quality relative to total received power |
| RS-[SINR](https://www.google.com/search?q=SINR+signal+interference+noise+ratio+LTE) | [dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit) | Signal-to-Interference-plus-Noise Ratio |
| Downlink Throughput | [Mbps](https://www.google.com/search?q=Mbps+megabits+per+second+data+rate) | Estimated DL data rate |
| Uplink Field Strength | dBm | Uplink signal level |
| UL SINR | dB | Uplink signal quality |
| UL Throughput | [Mbps](https://www.google.com/search?q=Mbps+megabits+per+second+data+rate) | Estimated UL data rate |
| Total DL Throughput | Mbps | Combined throughput from all best servers |

## Typical RSRP Thresholds

| RSRP (dBm) | Quality |
|---|---|
| > −80 | Excellent |
| −80 to −90 | Good |
| −90 to −100 | Fair |
| −100 to −110 | Poor (marginal outdoor) |
| < −110 | Very poor / no coverage |

## Viewing Results

1. In **Prediction History**, click the completed result row to load it on the map.
2. In the **Layers** panel, toggle between RSRP, SINR, Best Server, and Throughput views.
3. Click any point on the map to see the exact predicted value at that location.

## Prediction Models

Prediction models define how [path loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation) is calculated. Go to the **Prediction Models** tool to configure:

- Propagation formula (e.g. [Okumura-Hata](https://www.google.com/search?q=Okumura+Hata+propagation+model), Cost231, 3GPP)
- Frequency and band
- [Clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) loss coefficients (requires `clutterClasses.tif`)
- [Diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation) and morphology settings

Each model is assigned to a [workspace](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+workspace+project+geodatabase). You can have different models for different project areas.

## Related Pages

- [Quick Start Guide](../training/quick-start.md)
- [Publishing to Portal](publishing.md) — sharing results with your team
- [Geodata & Rasters](geodata.md)
- [Troubleshooting](troubleshooting.md)
