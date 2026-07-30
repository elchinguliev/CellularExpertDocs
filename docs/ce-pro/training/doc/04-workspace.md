# 04. Creating Workspace

> **Version:** CE Pro v4.9

## CE Pro Project Architecture

![Image p2](../../../assets/images/ce-pro/training-04/p002-img1.png)

A CE Pro project connects **ArcGIS Pro** to the Cellular Expert add-in and to your local workstation files:

- **Database** — the CE Pro workspace geodatabase
- **Geodata** — DTM, clutter, and obstacle rasters
- **Results** — prediction and analysis outputs

External data (ArcGIS Online, local files, or services) feeds into ArcGIS Pro, which the Cellular Expert add-in extends with RF planning tools.

## What Is a Workspace?

A CE Pro Workspace is a geodatabase (`.gdb`) that stores all project data — cells, sites, antennas, links, and prediction results. Every CE Pro project must have one workspace before any RF work can begin.

## CE Tools State

The **CE Tools** tab in the ArcGIS Pro ribbon shows one of three states:

**Workspace is not added** — no workspace linked to this project yet:

![Image p3](../../../assets/images/ce-pro/training-04/p003-img1.png)

**Workspace is added** — workspace found and geodata path is valid:

![Image p3](../../../assets/images/ce-pro/training-04/p003-img2.png)

**Workspace is added, but Geodata is missing** — workspace exists but the geodata folder path is broken:

![Image p3](../../../assets/images/ce-pro/training-04/p003-img3.png)

## Creating a New Workspace

When ArcGIS Pro opens, the start page lets you create a new project or open an existing one:

1. Open ArcGIS Pro and add a **Map** or **Local Scene** to your project
2. Click the **CE Desktop** tab in the ribbon
3. Click **Create Workspace**

![Image p4](../../../assets/images/ce-pro/training-04/p004-img1.png)

4. Fill in the required fields:

| Field | Description |
|---|---|
| New workspace path | Folder where the `.gdb` will be created |
| Geodata folder path | Path to your DTM / clutter / obstacle rasters |
| Projected coordinate system | Must match your geodata CRS (e.g., EPSG:3346 for Lithuania) |
| Also create Local Scene | Tick to add a 3D scene view automatically |

CE Pro validates the geodata as you enter the path — matched rasters and coordinate systems are confirmed in green, mismatches are flagged in red:

![Image p4](../../../assets/images/ce-pro/training-04/p004-img2.png)

![Image p4](../../../assets/images/ce-pro/training-04/p004-img3.png)

5. Click **Create** — CE Pro will build the geodatabase and populate it with the default schema

## Cellular Expert Project Structure

After creation, the workspace folder contains:

```
MyProject/
├── Predictions/          ← RF prediction output rasters
├── Results/               ← Processed result layers
├── SystemFiles/          ← Internal CE configuration files
├── Temp/                  ← Temporary calculation files
├── VolatileResults/      ← Short-lived result cache
├── VolatileTemp/          ← Short-lived temp cache
└── Workspace.gdb/         ← Main geodatabase (cells, sites, antennas, links)
```

The screenshots below show a populated workspace folder, including its Predictions, Results, and Temp job subfolders:

![Image p5](../../../assets/images/ce-pro/training-04/p005-img1.png)

![Image p5](../../../assets/images/ce-pro/training-04/p005-img2.png)

![Image p5](../../../assets/images/ce-pro/training-04/p005-img3.png)

![Image p5](../../../assets/images/ce-pro/training-04/p005-img4.png)

## Cellular Expert Dataset Objects

![Image p6](../../../assets/images/ce-pro/training-04/p006-img1.png)

The `Workspace.gdb` contains the following feature classes:

| Object | Description |
|---|---|
| Cell | Radio cell with RF parameters (frequency, power, antenna, technology) |
| Site | Physical mast or rooftop location grouping one or more cells |
| Radar | Radar interference source object |
| Repeater | Signal repeater / booster |
| CPE | Customer Premises Equipment (fixed wireless terminal) |
| OMEN | Omni-directional microwave node |
| Link | Point-to-point microwave or RL link |

## Changing Project Paths

If you move the geodata folder or the workspace after creation:

1. Click **CE Desktop → Workspace → Settings**
2. Update the **Geodata path** to the new location
3. Update **Calculation paths** (Predictions, Results, Temp) if needed
4. Click **Apply**

![Image p7](../../../assets/images/ce-pro/training-04/p007-img1.png)

## Project Settings and Rounding

Under **CE Desktop → Workspace → Project Settings** you can configure:

- Coordinate display format (decimal degrees vs projected metres)
- Power units (dBm / dBW)
- Distance units (km / miles)
- Rounding precision for displayed values

![Image p8](../../../assets/images/ce-pro/training-04/p008-img1.png)

## Workspace Upgrade

CE Pro automatically tracks the workspace database structure. When you open a workspace created with an older CE version, CE Pro detects a schema mismatch and prompts an upgrade:

1. Go to **CE Desktop → Workspace → Upgrade**
2. Review the list of new tables and fields that will be added
3. Click **Upgrade Database**

![Image p9](../../../assets/images/ce-pro/training-04/p009-img1.png)

![Image p9](../../../assets/images/ce-pro/training-04/p009-img2.png)

![Image p9](../../../assets/images/ce-pro/training-04/p009-img3.png)

> Upgrade is non-destructive — existing data is preserved. Always back up the `.gdb` before upgrading.

**Exercise:** `C:\CE_Course\0. Descriptions\1. Create workspace.pdf`

**Contact:** info@cellular-expert.com | +370 5 2150575 | www.cellular-expert.com
