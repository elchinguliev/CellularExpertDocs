# Antenna Patterns

An [antenna pattern](https://www.google.com/search?q=antenna+radiation+pattern+format) file describes how an antenna radiates power in different directions — both horizontally ([azimuth]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=antenna+azimuth+direction+degrees+north)) and vertically ([elevation]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=elevation+model+[terrain](https://www.google.com/search?q=terrain+elevation+model+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+topography)+height+datum)). [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) uses these patterns to calculate accurate RF predictions rather than assuming an idealised omnidirectional antenna.

## Supported Formats

| Format | Extension | Notes |
|---|---|---|
| [MSI Planet](https://www.google.com/search?q=MSI+Planet+antenna+pattern+format) | `.msi` | Most common format from antenna vendors |
| Kathrein | `.txt` | Text-based pattern format |

Most antenna manufacturers (Kathrein, Commscope, [Ericsson](https://www.google.com/search?q=Ericsson+telecom+network+vendor), Nokia, [Huawei](https://www.google.com/search?q=Huawei+telecom+network+equipment)) provide patterns in .msi format on their websites or on [Antenna DL](https://www.antenna-dl.com).

## Importing Antenna Patterns

1. Open the **Antennas** tool from the left toolbar.
2. Click **[Import](https://www.google.com/search?q=data+import+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format))**.
3. Select one or more `.msi` or `.txt` files.
4. Click **Open** — the patterns are imported into the antenna library.

You can [import](https://www.google.com/search?q=data+import+GIS+network+objects+[CSV](https://www.google.com/search?q=CSV+comma+separated+values+file+format)) multiple files at once. Imported patterns are available to all workspaces.

## Assigning a Pattern to a Cell

1. Open **Network Data Management**.
2. Find the [cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) row.
3. Click the `antenna_pattern` field.
4. Type or select the pattern name from the dropdown.
5. Click **Synchronize Changes**.

> If no pattern is assigned, [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) uses an **[isotropic](https://www.google.com/search?q=isotropic+antenna+radiator+reference) (omnidirectional)** model for that [cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station). This gives less accurate predictions but allows you to run a quick test without patterns.

## Pattern File Structure (MSI)

An .msi file contains:

- **Header** — frequency, gain, half-power beamwidths (H and V), front-to-back ratio
- **Horizontal pattern** — [attenuation](https://www.google.com/search?q=signal+attenuation+loss+radio+propagation) in [dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit) at each [azimuth](https://www.google.com/search?q=antenna+azimuth+direction+degrees+north) angle (0–360°)
- **Vertical pattern** — [attenuation](https://www.google.com/search?q=signal+attenuation+loss+radio+propagation) in [dB](https://www.google.com/search?q=dB+decibel+signal+measurement+unit) at each [elevation](https://www.google.com/search?q=elevation+model+[terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography)+height+datum) angle

Example header:
```
NAME    Kathrein 742212
MAKE    Kathrein
FREQUENCY   1710-1880
GAIN    17.5dBd
TILT    0
BEAMWIDTH H 65
BEAMWIDTH V 7.5
```

## Viewing Patterns

In the Antennas tool, click a pattern name to view its horizontal and vertical radiation plots.

## Managing the Antenna Library

| Action | How |
|---|---|
| View all imported patterns | Open Antennas tool → Library tab |
| Delete a pattern | Select the pattern → click Delete |
| [Export](https://www.google.com/search?q=data+export+GIS+raster+vector) a pattern | Select the pattern → click [Export](https://www.google.com/search?q=data+export+GIS+raster+vector) |
| Rename a pattern | Not supported — re-import under a new name |

## Tips

- Use the **actual vendor pattern** for your installed antennas whenever possible — it significantly improves prediction accuracy.
- Pattern file names often contain the model number (e.g. `K742212_1800MHz_0deg.msi`). Keep names consistent so they are easy to assign in bulk via CSV import.
- For multi-band antennas (e.g. 900/1800 [MHz](https://www.google.com/search?q=MHz+megahertz+frequency+unit) combined), import separate pattern files per band.

## Related Pages

- [Network Objects](network-objects.md) — assigning patterns to cells
- [RF Prediction](rf-prediction.md) — how patterns affect prediction results
