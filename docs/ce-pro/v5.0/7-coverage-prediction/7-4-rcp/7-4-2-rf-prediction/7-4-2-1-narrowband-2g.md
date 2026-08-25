# Narrowband 2G (GSM/CDMA-850/TETRA/P-25)

> **Applies to:** RCP.

Cells are automatically divided into sections based on the technology attribute. Select cells on the map and click the RF Prediction button to open the RF Prediction dialog — based on the selection, the cells are divided into technologies (Narrowband 2G, Broadband 3G, Broadband 4G, Broadband 5G, WiFi).

![RF Prediction dialog — technology selector with Narrowband 2G, Broadband 3G/4G/5G, and WiFi groups](../../../../../assets/images/ce-pro/v5.0/rf-prediction-technology-selector.png)

| Common Parameter | Description |
|---|---|
| Calculation Name | The name of the calculation will be displayed in the [CE Calculation Task List](../../7-1-ce-calculation-task-list.md). |
| Open raster after completion | Displays the prediction visualization (raster) after successful prediction calculation. |
| Recalculate Objection Position | Reviews the current X/Y and Longitude/Latitude values in the selected Cells table, and corrects them if these values differ from the object's geometry. |
| Calculate 3D | Runs calculations at different receiver heights and, after completion, creates a single Voxel file to visualize Field Strength values in a 3D scene. |
| Run | Starts the prediction calculation. |

## Narrowband 2G Parameters

![RF Prediction — Narrowband 2G (GSM/CDMA-850/TETRA/P-25) parameters panel](../../../../../assets/images/ce-pro/v5.0/rf-prediction-narrowband-2g-panel.png)

| Parameter | Description |
|---|---|
| Resolution | Resolution for raster calculations. The output rasters will be produced with the indicated cell size. |
| Best server count | Option to calculate up to 5 best servers. The prediction rasters show the 1st, 2nd, 3rd, and so on strongest signal sources. |
| Cell Template | Option to use the parameters from the template if the cell misses the required parameters. |
| Repeater Template | Option to use the parameters from the template if repeaters are selected and they are missing the required parameters. |
| Calculate Technology Totals | Combines all resulting Field Strength rasters into a singular Field Strength raster. |
| Calculate Uplink | Option to calculate the Uplink signal strength. |
| RX EIRP, dBm | The power that the receiving antenna can capture from the transmitted signal, in dBm. |
| Calculate Interference | Calculates the interference for 2G cells. For this calculation, the C/I and C/A thresholds must be defined. |
| C/I Max Field Margin, dB | The corresponding channel's signal interference if the first and the second strongest signals differ by less than or equal to 10 dBm. |
| C/A Max Field Margin, dB | The neighboring channel's signal interference if the first and the second strongest signals differ by less than or equal to 10 dBm. |
| Calculate Neighbours | Enables cell neighbour matrix calculation. |

### Calculate Neighbours

Neighbour relationships between cells are determined based on:

- **Minimum FS threshold (dBm)** — ensures neighbours are only counted if they meet a minimum signal level.
- **Neighbour minimum coverage (%)** — sets the minimum overlap percentage required for a cell to qualify as a neighbour.
- **Maximum neighbour count** — limits the number of neighbours assigned to each cell.

The results include a visual neighbour matrix showing connections between cells with coloured link lines.

![Neighbour matrix — colored link lines connecting cells, with Relation type, Frequency group, Overlap area/percentage](../../../../../assets/images/ce-pro/v5.0/rf-prediction-neighbour-matrix.png)

For each calculated cell:

- Frequency group (MHz)
- Covered area (km²)
- Neighbouring cells with:
  - Relation type (e.g. Intra-Frequency)
  - Overlap area (in km²)
  - Overlap percentage (%)

## Available Coverage Rasters

- Received signal level raster in dBm, within the channel bandwidth appropriate to this technology. It is possible to calculate separately the rasters for the 1st, 2nd, 3rd, 4th, and 5th strongest signal levels, depending on the count defined in the Best server count option.
- The best server raster shows the identification of cells generating the strongest signals at each pixel. Raster count depends on the Best server count parameter value specified by the user:
  - 1st best server shows the serving cell with the strongest field strength.
  - 2nd best server shows the second strongest field strength cell identification.
  - 3rd best server shows the third strongest field strength cell identification.
  - 4th best server shows the fourth strongest field strength cell identification.
  - 5th best server shows the fifth strongest field strength cell identification.
- C/I raster shows the Carrier-to-Interference ratio in dB, to account for inter-cell interference from nearby cells that utilize the same carrier.
- C/A raster shows the Carrier-to-Adjacent interference ratio in dB, to account for inter-cell interference from nearby cells that operate the adjacent carrier (adjacent frequency channel).
- Uplink Field Strength raster shows receiver signal strength in dBm.

![Example field strength coverage raster over a wide area with multiple cell sites](../../../../../assets/images/ce-pro/v5.0/rf-prediction-coverage-result-example.png)
