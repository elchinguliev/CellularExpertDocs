# 09. Preparing Geodata

1. Objective
This module explains how to prepare topographical and land-use geodata in [ArcGIS Pro](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+Pro+Esri+desktop+software) so
it can be correctly used for predictions in [CE Express]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) or [CE Desktop]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Desktop+[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+Pro) for [ArcGIS Pro](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+platform)+Pro+Esri+desktop+software). The
focus is on producing rasters that are geometrically correct, consistently referenced, and
compliant with CE input requirements.
By the end of this exercise, participants will be able to:
- Understand which geodata layers are mandatory and optional for [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform)
- Prepare a [Digital [Terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) Model](https://www.google.com/search?q=Digital+[Terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography)+Model+[DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation+data)+bare+earth) ([DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model)) [raster](https://www.google.com/search?q=raster+GIS+grid+data+format) suitable for predictions
- Mosaic, project, and standardize [raster](https://www.google.com/search?q=raster+GIS+grid+data+format) datasets in [ArcGIS Pro](https://www.google.com/search?q=ArcGIS+Pro+Esri+desktop+software)
- Prepare [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio) class and [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) height rasters aligned with the [DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation+data)
- [Export](https://www.google.com/search?q=data+export+GIS+raster+vector) final rasters with correct naming, [resolution](https://www.google.com/search?q=spatial+resolution+raster+GIS+accuracy), extent, and data type
2. Required and Optional Geodata Layers
Mandatory. [Digital terrain model](https://www.google.com/search?q=Digital+Terrain+Model+DTM+bare+earth) (DTM) grid
The Digital Terrain Model (DTM) represents the Earth’s ground level above sea level. Each
raster [pixel](https://www.google.com/search?q=pixel+raster+grid+[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+resolution) has its height value. Freely available data can be download from:
https://search.earthdata.nasa.gov/search/granules?p=C1711961296-LPCLOUD&pg[0][v]=f&pg[0][gsk]=-start_date&g=G1726517680-
LPCLOUD&q=[aster](https://www.google.com/search?q=ASTER+[DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster)+NASA+global+elevation+model)&lat=54.10244930917067&long=26.561757102638634&zoom=6.73700
5077561119
The raster name must be [elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum).tif

---

Optional. [Clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) height grid
The Obstacle height (building, vegetation, etc) grid represents the objects on the ground
with their height above the DTM grid. The raster name must be clutterHeight.tif
Optional. Clutter class grid
A Clutter class grid represents [land use](https://www.google.com/search?q=land+use+land+cover+classification+GIS) types. The data can be downloaded from here:
Livingatlas ArcGIS [Sentinel-2](https://www.google.com/search?q=Sentinel+2+ESA+satellite+land+cover) [Land Use](https://www.google.com/search?q=land+use+land+cover+classification+GIS)

---

Possible land use types:
- Water
- Tress
- Flooded vegetation
- Crops
- Built area
- Snow/Ice
- Rangeland
The clutter must be named clutterClasses.tif.
3. Exercise

## 3.1 Step 1 – Opening the ArcGIS Pro Project

1. Navigate to:
C:\CE_Course\PreparingGeodata\Project
2. Open the ArcGIS Pro project file:
Project.aprx
This project contains predefined folder structures and basemaps used throughout the
exercise.

## 3.2 Step 2 – Preparing the Digital Terrain Model (DTM)

3.2.1 Adding Source DTM Tiles
1. Click Add Data.
2. Navigate to:
C:\CE_Course\PreparingGeodata\Initial\DTM
3. Select the following files:

---

- ASTGTMV003_N54E024_dem.tif
- ASTGTMV003_N54E025_dem.tif
4. Click OK.
These files represent adjacent DTM tiles and must be merged into a single raster.
3.2.2 Mosaic to New Raster
1. Open Geoprocessing from the View tab.
2. In Find Tools, search for Mosaic to New Raster.
3. Configure the tool as shown in the training reference:
- Input Rasters: both [ASTER](https://www.google.com/search?q=ASTER+[DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster)+NASA+global+elevation+model) tiles
- Output location: calculation directory
- Output raster name: temporary DTM

---

4. Click Run.
This creates a single continuous [elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum) raster.

## 3.3 Project raster

Projecting the Digital Terrain Model (DTM) is a critical GIS step that ensures the elevation
data can be correctly interpreted and used by CE. Prediction engines require all geodata to

---

be in a [projected coordinate](https://www.google.com/search?q=projected+coordinate+system+[UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator+projection)+GIS) system so that distances, angles, and areas are calculated
accurately.
Raster datasets provided in [geographic coordinate](https://www.google.com/search?q=geographic+coordinate+system+latitude+longitude) systems (latitude/longitude) are not
suitable for prediction calculations without reprojection, because their units are angular rather
than linear.
3.3.1 Selecting the Correct [Coordinate System](https://www.google.com/search?q=coordinate+reference+system+CRS+GIS)
Before projecting, determine the most appropriate [projected coordinate](https://www.google.com/search?q=projected+coordinate+system+[UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator+projection)+GIS) system:
- Local / National grid systems are preferred when available (e.g. LKS 1994
Lithuania TM)
- WGS 1984 [UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator) zones are suitable when national systems are not available
When using UTM:
- Select the zone covering the majority of the study area
- Avoid splitting datasets across multiple UTM zones
Which zone should be used can be checked https://hub.arcgis.com/datasets/esri::world-utm-grid/explore
Consistency across all geodata layers is mandatory.

---

3.3.2 Running the Project Raster Tool
1. Open Geoprocessing from the View tab.
2. Search for Project Raster.
Configure the tool as follows:
- Input raster: DTM_WGS.tif
- Output Raster Dataset:
C:\CE_Course\PreparingGeodata\Initial\Calculations\DTM_UTM.tif
- LKS_1994_Lithuania_TM
- [Cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) size:
o X: 25
o Y: 25

---

Run calculations.
3.3.3 Finalizing the Elevation Raster
1. Open Copy Raster.
Define:
- Input raster: projected DTM
- Output raster: elevation.tif
- [Pixel](https://www.google.com/search?q=pixel+raster+grid+cell+resolution) Type: 16-bit signed, 32-bit signed, or 32-bit float
- [NoData](https://www.google.com/search?q=NoData+raster+value+GIS+missing+data) value: -9999
3. Click Run.
4. Remove all other layers except:
- elevation.tif

---

- Topographic basemap
The DTM is now ready for CE Express.

## 3.4 Step 3 – Preparing Clutter Class Raster

The clutter class raster is downloaded from here:
https://livingatlas.arcgis.com/landcoverexplorer/?hsamp_network=linkedin&hsamp=bMJ1Ld
VdwXGW&adumkts=social&utm_source=social&aduc=social&adum=external&adusf=linke
din&sf_id=7015x000000aYlKAAU&aduca=mi_employee_advocacy_hootsuite_amplify_soc
_ex&adut=e621d967-b85a-4721-aa1e-d37a8f477f1b#mapCenter=-
3.96366%2C55.51588%2C4.00&mode=step&timeExtent=2017%2C2022&year=2024&dow
nloadMode=true
3.4.1 Adding Clutter Class Data
1. Click Add Data.
2. Navigate to:
C:\CE_Course\PreparingGeodata\Initial\Clutter
3. Select:
35U_20240101-20241231.tif

---

4. Click OK.
This raster covers a much larger area than the DTM.
3.4.2 Projecting and Clipping Clutter Classes
Clutter class rasters must match the DTM in all spatial aspects. Any mismatch can lead to
incorrect obstruction modeling and unstable prediction results.
Proper [projection](https://www.google.com/search?q=map+projection+coordinate+system+GIS) and clipping ensures:
- Correct spatial alignment between terrain and clutter
- One-to-one pixel correspondence across rasters
- Consistent distance and area calculations
- Reliable application of clutter loss models
3.4.3 Reprojecting the Clutter Class Raster
1. Open Geoprocessing in ArcGIS Pro.
2. Search for Project Raster.
Configure the tool as follows:
- Input Raster: Original clutter class dataset
- Output Raster: C:\CE_Course\PreparingGeodata\Initial\Calculations\clutter_UTM.tif
- Output [Coordinate System](https://www.google.com/search?q=coordinate+reference+system+CRS+GIS): Same projected system used for elevation.tif

---

3.4.4 Enforcing Spatial Alignment (Environment Settings)
To ensure perfect alignment with the DTM, configure the Environment settings before
running the tool:
- Processing Extent: Same as elevation.tif
- Snap Raster: elevation.tif
These settings force ArcGIS Pro to:
- Clip the raster to the exact DTM extent
- Align pixel boundaries exactly with the DTM grid

---

Press Run.
3.4.5 Finalizing the Clutter Class Raster
1. Open Copy Raster.
2. Configure:
- Output name: clutterClasses.tif
- Pixel Type: 32-bit signed integer
- [NoData](https://www.google.com/search?q=NoData+raster+value+GIS+missing+data) value: -9999
3. Click Run.
4. Remove all intermediate clutter rasters from the map.
The clutter class raster is now fully prepared and compliant with CE requirements.

---
