# 01. Data Types

Data Types
Data can be:
1. [Vector]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=vector+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+shapefile+feature+data)
- Points
- Lines
- Polygons
2. [Raster]([https](https://www.google.com/search?q=HTTPS+[SSL](https://www.google.com/search?q=SSL+Secure+Sockets+Layer+encryption)+[TLS](https://www.google.com/search?q=TLS+Transport+Layer+Security)+secure+protocol)://www.google.com/search?q=raster+[GIS](https://www.google.com/search?q=GIS+Geographic+Information+System)+grid+data+format)
- [GeoTIFF](https://www.google.com/search?q=GeoTIFF+raster+geospatial+format)
3. Tabular

---

Modelling Outdoor coverage
The CE tools make use of three distinct [GIS](https://www.google.com/search?q=GIS+Geographic+Information+System) data layers to obtain high
precision modelling of radio [wave propagation](https://www.google.com/search?q=radio+wave+propagation+physics) losses:
1. [Digital [Terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography) Model](https://www.google.com/search?q=Digital+[Terrain](https://www.google.com/search?q=terrain+elevation+model+GIS+topography)+Model+[DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation+data)+bare+earth) ([DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model)), also known as Digital [Elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum)
Model ([DEM](https://www.google.com/search?q=DEM+Digital+Elevation+Model+terrain)), which describes Earth surface, i.e., path terrain
profile in terms of ground [elevation](https://www.google.com/search?q=elevation+model+terrain+height+datum) above uniform sea level.
2. Obstacles layer, delineating buildings and other such objects
above Earth surface that may be considered to be principal
impediments for radio [wave propagation](https://www.google.com/search?q=radio+wave+propagation+physics).
3. [Clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) layer, delineating natural occurring or human cultivated
ground cover that may be partially penetrable by radio waves,
such as natural vegetation (e.g., forests, trees, bushes) or various
crops, gardens, parks, etc.
[Diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation) Free Space Loss
[Diffraction](https://www.google.com/search?q=radio+diffraction+obstacle+propagation)
H
obstacles
H
[Clutter](https://www.google.com/search?q=clutter+land+use+classification+radio+planning) losses [clutter](https://www.google.com/search?q=clutter+land+use+classification+radio) [DSM](https://www.google.com/search?q=DSM+Digital+Surface+Model)
UE
[DTM](https://www.google.com/search?q=DTM+Digital+Terrain+Model+elevation+data)

---

[Raster](https://www.google.com/search?q=raster+GIS+grid+data+format) Type Input: Elevation
- [Digital terrain model](https://www.google.com/search?q=Digital+Terrain+Model+DTM+bare+earth) (DTM)
- Represents Earth’s ground/water level above sea level
- [GeoTIFF](https://www.google.com/search?q=GeoTIFF+raster+geospatial+format) raster format
- Height values in meters
- [Coordinate system](https://www.google.com/search?q=coordinate+reference+system+CRS+GIS) – projected
- [Resolution](https://www.google.com/search?q=spatial+resolution+raster+GIS+accuracy) ([cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) size) – centimeter level
- Raster name: elevation.tif

---

Raster Type Input: Clutter height
- Clutter height
- Represents objects height above elevation raster.
- [GeoTIFF](https://www.google.com/search?q=GeoTIFF+raster+geospatial+format) raster format
- Height values in meters
- [Coordinate system](https://www.google.com/search?q=coordinate+reference+system+CRS+GIS) – projected
- [Resolution](https://www.google.com/search?q=spatial+resolution+raster+GIS+accuracy) ([cell](https://www.google.com/search?q=mobile+cell+sector+coverage+base+station) size) – centimeter level
- Raster name: clutterHeight.tif

---

DTM vs. Surface
Tx
Visible
Rx
Visible
Rx
Surface grid
Tx
Obstacles grid
Visible Not visible
Rx Rx
Elevation grid

---

Clutter classes
- Clutter classes
- Represents [land use](https://www.google.com/search?q=land+use+land+cover+classification+GIS) classes.
- GeoTIFF raster format
- Coordinate system – projected
- Resolution (cell size) – centimeter level
- Raster name: clutterClasses.tif

---

Clutter types
Corine [Land Cover](https://www.google.com/search?q=land+cover+classification+satellite+imagery)

---

Raster from [vector](https://www.google.com/search?q=vector+GIS+shapefile+feature+data) data
Following should be defined: input layer,
output raster cell size, data field that will be
converted to grid, output raster file name.
Note: if some features in input layer are selected,
only selected ones will be converted.

---

Environment Settings

---

Raster Calculator

---

Model Builder
Automate your GIS tasks

---

Questions?
www.cellular-expert.com

---
