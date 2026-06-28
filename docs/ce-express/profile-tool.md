# Path Profile & __S2__

The **Profile** tool analyses the [terrain]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography) between two points — typically between a transmitter ([cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)) and a receiver location. It shows whether a clear [line of sight]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=Line+of+Sight+[LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation)+radio+propagation) exists, how much [Fresnel zone](https://www.google.com/search?q=Fresnel+zone+radio+link+clearance) clearance there is, the expected [path loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation), and the link power budget.

## When to Use the Profile Tool

- Checking whether a [microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning) link has sufficient clearance
- Verifying that a [cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) has [line-of-sight](https://www.google.com/search?q=line+of+sight+[LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation)+radio+link) to a target location
- Estimating [path loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit)) for a specific [point-to-point](https://www.google.com/search?q=point+to+point+radio+link+[microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning)) link
- Planning [repeater](https://www.google.com/search?q=radio+repeater+signal+booster+telecom) placement (finding obstructions)

## Running a Profile

1. Open the **Profile** tool from the left toolbar.

2. **Set the transmitter** — hold **CTRL** and click on a cell on the map. The tool snaps to the cell and reads its position and height.

3. **Set the receiver** — left-click a point on the map. The profile calculates automatically.

4. The **Profile panel** appears showing:
   - A [terrain](https://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography) cross-section graph between the two points
   - First [Fresnel zone](https://www.google.com/search?q=Fresnel+zone+radio+link+clearance+calculation) ellipse overlay
   - Summary results table

## Understanding the Results

| Result | Description |
|---|---|
| **Clearance** | How much of the first [Fresnel zone](https://www.google.com/search?q=Fresnel+zone+radio+link+clearance+calculation) is clear of obstacles (%). ≥ 60% is acceptable; ≥ 100% is ideal. |
| **Power Budget** | Received signal power at the receiver ([dBm](https://www.google.com/search?q=dBm+decibel+milliwatt+power+unit)), accounting for [path loss](https://www.google.com/search?q=path+loss+radio+signal+attenuation+[dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit)), [antenna gain](https://www.google.com/search?q=antenna+gain+[dBi](https://www.google.com/search?q=dBi+decibel+isotropic+antenna+gain)+directional), and cable loss |
| **Path Loss** | Total signal [attenuation](https://www.google.com/search?q=signal+attenuation+loss+radio+propagation) between transmitter and receiver (dB) |
| **Angle** | [Elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum) angle from transmitter to receiver (degrees) |
| **Distance** | Straight-line distance between the two points |

## Fresnel Zone Clearance

The Fresnel zone is an elliptical region around the direct path between two antennas. Signal energy travels not just along the direct line but also through this zone. Obstructions inside the Fresnel zone cause [diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation) losses:

| Clearance | Effect |
|---|---|
| > 100% | Full clearance, minimal [diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation) loss |
| 60–100% | Minor diffraction loss (< 1 dB typical) |
| < 60% | Significant diffraction loss — consider adjusting antenna heights or finding an alternative path |
| 0% (obstructed) | Non-[line-of-sight](https://www.google.com/search?q=line+of+sight+LOS+radio+link) ([NLOS](https://www.google.com/search?q=NLOS+Non+Line+of+Sight+radio+propagation)) — may still work but with higher loss |

## Reading the Profile Graph

The graph shows:
- **Brown/grey area** — terrain [elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum) along the path
- **Dashed ellipse** — first Fresnel zone boundary
- **Red line** — direct path between transmitter and receiver
- **Obstructions** — terrain or [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio) features that intersect the Fresnel zone are highlighted

## Tips

- Hold **CTRL** when clicking on any [network object](https://www.google.com/search?q=radio+network+object+GIS+database) to snap precisely to its position (useful for both ends of a microwave link).
- For **microwave link planning**, use the Profile tool before ordering equipment to confirm clearance at different frequencies (the Fresnel zone radius changes with frequency).
- The profile uses the `elevation.tif` terrain model, and `clutterHeight.tif` if available, to account for buildings and trees.
- To compare multiple paths, run the profile tool multiple times — each result is shown in the panel as a separate tab.

## Related Pages

- [Geodata & Rasters](geodata.md) — the terrain data used by the profile tool
- [CE Desktop RLP](../ce-desktop/rlp.md) — detailed microwave [link budget](https://www.google.com/search?q=link+budget+microwave+radio+calculation) planning
- [Network Objects](network-objects.md) — setting correct antenna heights for accurate profiles
