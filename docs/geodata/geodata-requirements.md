# Geodata Requirements 2025

Cellular Expert Technical Documentation
Table of Contents
1. High-Precision Inputs and Next-Generation Propagation 3
2. Geographic data requirements 5

## 2.1 Digital Terrain Model (__S0__) Grid (Mandatory) 5

2.1.1 [Projection]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=map+projection+coordinate+system+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)) 6
2.1.2 Correct No Data value and [raster]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=raster+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+grid+data+format) name 6
2.1.3 [Pixel](https://www.google.com/search?q=pixel+raster+grid+[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+resolution) type 6

## 2.2 Clutter classes grid (optional) 7

2.2.1 [Projection](https://www.google.com/search?q=map+projection+coordinate+system+GIS) 8
2.2.2 Correct No Data value and [raster](https://www.google.com/search?q=raster+GIS+grid+data+format) name 8
2.2.3 [Pixel](https://www.google.com/search?q=pixel+raster+grid+[cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station)+resolution) type 8

## 2.3 Clutter heights (optional) 8

2.3.1 Projection 10
2.3.2 Correct No Data value and raster name 10
2.3.3 Pixel type 10
©Cellular Expert, 2025 Page | 2

---

Cellular Expert Technical Documentation
1. High-Precision Inputs and Next-Generation Propagation
[CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) is designed to work with any geospatial data available to the customer and fully exploit its
precision for the most accurate coverage and QoS calculations. The platform supports multi-[resolution](https://www.google.com/search?q=spatial+resolution+raster+GIS+accuracy) input
datasets — from freely available global sources such as [Sentinel-2](https://www.google.com/search?q=Sentinel+2+ESA+satellite+land+cover) 10 m [land cover](https://www.google.com/search?q=land+cover+classification+satellite+imagery) and [ASTER](https://www.google.com/search?q=ASTER+[DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster)+NASA+global+elevation+model) [DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain), to
premium high-[resolution](https://www.google.com/search?q=spatial+resolution+raster+GIS+accuracy) [terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) and [3D building](https://www.google.com/search?q=3D+building+model+urban+GIS) models when provided by the customer or government
agencies.
Source: https://livingatlas.[arcgis](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform).com/landcoverexplorer/
By leveraging whatever data is available locally, [CE Express](https://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) performs nationwide calculations at the
maximum feasible resolution, accurately modeling [signal propagation](https://www.google.com/search?q=signal+propagation+radio+wave) even in dense urban environments.
Support for 3D multi-height calculations ensures that coverage predictions reflect street-level, indoor, and
rooftop conditions, providing regulators with a realistic representation of service [availability](https://www.google.com/search?q=link+availability+percentage+[microwave](https://www.google.com/search?q=microwave+[backhaul](https://www.google.com/search?q=backhaul+microwave+telecom+network)+radio+link+planning)+ITU).
This flexibility ensures that customers can use their existing [GIS](https://www.google.com/search?q=GIS+Geographic+Information+System) assets, open datasets, or commercial data
they already license, turning them into actionable broadband maps without additional data procurement
requirements from the solution provider.
By using [terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) [elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum), obstacles, and [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio) classification in every calculation, Cellular Expert
accurately models:
- [Line-of-Sight](https://www.google.com/search?q=line+of+sight+[LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation)+radio+link) and Non-[Line-of-Sight](https://www.google.com/search?q=line+of+sight+[LOS](https://www.google.com/search?q=LOS+Line+of+Sight+radio+propagation)+radio+link) Conditions – Determining [diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation), [reflection](https://www.google.com/search?q=radio+wave+reflection+[multipath](https://www.google.com/search?q=multipath+propagation+fading+radio)), and
shadowing effects over hills, valleys, and urban obstacles.
- Coverage Footprints – Generating precise signal strength maps at national, regional, and local
levels.
- [Capacity](https://www.google.com/search?q=network+capacity+planning+telecom) and [Interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent) Analysis – Modeling realistic signal overlaps and [interference](https://www.google.com/search?q=radio+interference+co+channel+adjacent) zones
for multi-operator, multi-technology environments.
©Cellular Expert, 2025 Page | 3

---

Cellular Expert Technical Documentation
Diffractio Free Space Loss
n
Diffractio
H
H [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) n obstacles
[DSM](https://www.google.com/search?q=DSM+Digital+Surface+Model)
[Clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) losses
UE
[DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation+data)
The CE tools make use of three distinct GIS data layers to obtain high precision modelling of radio wave
propagation losses:
- [Digital Terrain Model](https://www.google.com/search?q=Digital+Terrain+Model+[DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation+data)+bare+earth) (DTM), also known as [Digital [Elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum) Model](https://www.google.com/search?q=Digital+Elevation+Model+[DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain+raster)+terrain+data) (DEM), which describes
Earth surface, i.e., path [terrain profile](https://www.google.com/search?q=terrain+profile+elevation+radio+link) in terms of ground elevation above uniform sea level.
- Obstacles layer, delineating buildings and other such objects above Earth surface that may be
considered to be principal impediments for radio [wave propagation](https://www.google.com/search?q=radio+wave+propagation+physics).
- Clutter layer, delineating natural occurring or human cultivated ground cover that may be
partially penetrable by radio waves, such as natural vegetation (e.g., forests, trees, bushes) or
various crops, gardens, parks, etc.
The image above illustrates how Cellular Expert uses different resolutions of topographical data to
significantly improve [coverage prediction](https://www.google.com/search?q=coverage+prediction+RF+radio+planning) accuracy.
- Left image: Coverage calculated using 25 m resolution [ASTER](https://www.google.com/search?q=ASTER+DEM+NASA+global+elevation+model) DEM data, showing a general view
of signal distribution but with limited detail, especially in dense urban areas.
- Right image: Coverage calculated using 1 m resolution data, revealing a much more precise
propagation pattern, including building-level shadowing and accurate street-by-street coverage.
More information: https://blog.maxar.com/earth-intelligence/2022/benefits-of-using-maxars-precision3d-telco-suite-for-[5g](https://www.google.com/search?q=5G+fifth+generation+mobile+network)
Cellular Expert can easily integrate and process 1 m or even sub-meter topographical data, providing highly
detailed RF calculations. This level of precision is essential for:
- Modeling [2G](https://www.google.com/search?q=2G+GSM+mobile+network+second+generation)/[3G](https://www.google.com/search?q=3G+UMTS+HSPA+mobile+network)/[4G](https://www.google.com/search?q=4G+LTE+mobile+network+technology)/[5G](https://www.google.com/search?q=5G+fifth+generation+mobile+network), small cells and mmWave networks.
- Identifying exact coverage gaps at the building and street level.
©Cellular Expert, 2025 Page | 4

---

Cellular Expert Technical Documentation
- Supporting regulatory-grade broadband mapping and planning.
By using high-resolution terrain and clutter data, Cellular Expert ensures that its calculations match real-
world conditions as closely as possible — resulting in better network design decisions and more reliable
broadband planning outcomes.
2. Geographic data requirements
The supported geographical data types:
Only [GeoTIFF](https://www.google.com/search?q=GeoTIFF+raster+geospatial+format) is supported. Topographical data must have specific names:
- The [Digital terrain model](https://www.google.com/search?q=Digital+Terrain+Model+DTM+bare+earth) must be named elevation.tif
- The [land use](https://www.google.com/search?q=land+use+land+cover+classification+GIS) (or clutter) grid must be named clutterClasses.tif
- The clutter heights (typically building, vegetation height) grid must be named clutterHeight.tif
Mandatory geographical data:
- Digital Terrain Model (DTM) grid
All geodata must be located in one catalog.

## 2.1 Digital Terrain Model (DTM) Grid (Mandatory)

The Digital Terrain Model (DTM), also known as [Digital Elevation Model](https://www.google.com/search?q=Digital+Elevation+Model+DEM+terrain+data) (DEM), represents the Earth’s
ground level above sea level. Each raster pixel has its height value.
A sample DTM raster is presented below. Each pixel represents height value above the sea level. In reality,
within a one-pixel area, the height is not the same everywhere. Thus, the pixel’s height value is the height
©Cellular Expert, 2025 Page | 5

---

Cellular Expert Technical Documentation
in its center or the maximum. The smaller the pixels, the more accurate is the grid - but also more data to
calculate.
2.1.1 Projection
The raster must use a [Projected Coordinate](https://www.google.com/search?q=projected+coordinate+system+[UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator+projection)+GIS) System. To check the [coordinate system](https://www.google.com/search?q=coordinate+reference+system+CRS+GIS) of your raster, use
the Properties function in [ArcGIS Pro](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+Pro+Esri+desktop+software). Add the raster to your project, right-click on it, and select Properties.
Then, go to the Source tab > Spatial Reference and check the [Coordinate System](https://www.google.com/search?q=coordinate+reference+system+CRS+GIS) type parameter to confirm
it is in a [Projected Coordinate](https://www.google.com/search?q=projected+coordinate+system+[UTM](https://www.google.com/search?q=UTM+Universal+Transverse+Mercator+projection)+GIS) System.
2.1.2 Correct No Data value and raster name
After setting the correct projection, assign the [NoData](https://www.google.com/search?q=NoData+raster+value+GIS+missing+data): -9999 attribute and specify the appropriate name for
the DTM raster.
2.1.3 Pixel type
16-bit signed, or 32-bit signed or 32-bit float
©Cellular Expert, 2025 Page | 6

---

Cellular Expert Technical Documentation

## 2.2 Clutter classes grid (optional)

[Land use](https://www.google.com/search?q=land+use+land+cover+classification+GIS) or clutter refers to the classification of the earth’s surface into categories such as urban, suburban,
rural, forest, water, and open land, each of which affects radio propagation differently. Clutter data is crucial
because it determines how signals are absorbed, reflected, or diffracted by the environment, directly
influencing coverage, interference, and quality of service. The naming and classification of land use types
may vary. An example is the [Sentinel-2](https://www.google.com/search?q=Sentinel+2+ESA+satellite+multispectral+imagery) [Land Cover](https://www.google.com/search?q=land+cover+classification+satellite+imagery) dataset from the Living Atlas: Living Atlas [Sentinel-2](https://www.google.com/search?q=Sentinel+2+ESA+satellite+multispectral+imagery)
Land Cover
©Cellular Expert, 2025 Page | 7

---

Cellular Expert Technical Documentation
2.2.1 Projection
The raster must use a Projected Coordinate System. To check the coordinate system of your raster, use
the Properties function in [ArcGIS Pro](https://www.google.com/search?q=[ArcGIS](https://www.google.com/search?q=ArcGIS+Esri+GIS+platform)+Pro+Esri+desktop+software). Add the raster to your project, right-click on it, and select Properties.
Then, go to the Source tab > Spatial Reference and check the Coordinate System type parameter to confirm
it is in a Projected Coordinate System.
2.2.2 Correct No Data value and raster name
After setting the correct projection, assign the [NoData](https://www.google.com/search?q=NoData+raster+value+GIS+missing+data): -9999 attribute and specify the appropriate name for
the DTM raster.
2.2.3 Pixel type
16-bit signed, or 32-bit signed or 32-bit float

## 2.3 Clutter heights (optional)

Clutter heights represent the vertical dimension of obstacles such as buildings, trees, and other surface
features above the digital terrain model (DTM). While the DTM provides the bare-earth elevation, clutter
heights add the true 3D profile of the environment by capturing how high objects rise above the ground.
The clutter heights raster requires the accompanying clutterClasses.tif raster and cannot be used
independently.
©Cellular Expert, 2025 Page | 8

---

Cellular Expert Technical Documentation
A clutter height raster can be derived from a [Digital Surface Model](https://www.google.com/search?q=Digital+Surface+Model+[DSM](https://www.google.com/search?q=DSM+Digital+Surface+Model+buildings+trees)+buildings) ([DSM](https://www.google.com/search?q=DSM+Digital+Surface+Model+buildings+trees)) raster and a Digital Terrain Model
(DTM) raster using the ArcGIS Raster Calculator tool.
The calculation output will be the difference between the DSM and DTM grids, representing the clutter
heights.
©Cellular Expert, 2025 Page | 9

---

Cellular Expert Technical Documentation
2.3.1 Projection
The raster must use a Projected Coordinate System. To check the coordinate system of your raster, use
the Properties function in [ArcGIS Pro](https://www.google.com/search?q=ArcGIS+Pro+Esri+desktop+software). Add the raster to your project, right-click on it, and select Properties.
Then, go to the Source tab > Spatial Reference and check the Coordinate System type parameter to confirm
it is in a Projected Coordinate System.
2.3.2 Correct No Data value and raster name
After setting the correct projection, assign the NoData: -9999 attribute and specify the appropriate name for
the DTM raster.
2.3.3 Pixel type
16-bit signed, or 32-bit signed or 32-bit float
©Cellular Expert, 2025 Page | 10

---
