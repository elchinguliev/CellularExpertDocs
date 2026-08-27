# Data Types

All CE Pro data — sites, cells, prediction rasters, and geodata layers — is displayed in the ArcGIS Pro map view:

Geodata layers and network feature classes are managed in the **Contents** and **Catalog** panes:

## Data Types

Data can be:

1. **Vector**
   - Points

     ![Vector points example](../../assets/images/ce-pro/training-01/p002-img1.png)
   - Lines

     ![Vector lines example](../../assets/images/ce-pro/training-01/p002-img2.png)
   - Polygons

     ![Vector polygons example](../../assets/images/ce-pro/training-01/p002-img3.png)
2. **Raster**
   - GeoTIFF

     ![GeoTIFF raster example](../../assets/images/ce-pro/training-01/p002-img4.png)
3. **Tabular**

   ![Tabular data example](../../assets/images/ce-pro/training-01/p002-img5.png)

## Modelling Outdoor Coverage

The CE tools make use of three distinct GIS data layers to obtain high precision modelling of radio wave propagation losses:

1. **Digital Terrain Model** (DTM), also known as Digital Elevation Model (DEM), which describes Earth surface, i.e., path terrain profile in terms of ground elevation above uniform sea level.
2. **Obstacles layer**, delineating buildings and other such objects above Earth surface that may be considered to be principal impediments for radio wave propagation.
3. **[Clutter](#kw:clutter-classification-values:ce-express-geodata) layer**, delineating natural occurring or human cultivated ground cover that may be partially penetrable by radio waves, such as natural vegetation (e.g., forests, trees, bushes) or various crops, gardens, parks, etc.

![Propagation loss diagram — clutter losses, diffraction, free space loss, DSM, and DTM](../../assets/images/ce-pro/training-01/p003-img2.png)

![CE Pro coverage prediction map with elevation, buildings, and clutter profile](../../assets/images/ce-pro/training-01/p003-img24.png)

## Raster Type Input: Elevation

- **Digital terrain model (DTM)**
  - Represents Earth's ground/water level above sea level
  - GeoTIFF raster format
  - Height values in meters
  - Coordinate system – projected
  - Resolution (cell size) – centimeter level
  - Raster name: elevation.tif

![elevation.tif legend](../../assets/images/ce-pro/training-01/p004-img2.png)

![Elevation raster example](../../assets/images/ce-pro/training-01/p004-img1.png)

## Raster Type Input: Clutter Height

- **Clutter height**
  - Represents objects height above elevation raster.
  - GeoTIFF raster format
  - Height values in meters
  - Coordinate system – projected
  - Resolution (cell size) – centimeter level
  - Raster name: clutterHeight.tif

![obstacle_height.tif legend](../../assets/images/ce-pro/training-01/p005-img2.png)

![Clutter height raster example](../../assets/images/ce-pro/training-01/p005-img1.png)

## DTM vs. Surface

![Diagram comparing surface grid, obstacles grid, and elevation grid visibility between Tx and Rx](../../assets/images/ce-pro/training-01/p006-img1.png)

## Clutter Classes

- **[Clutter classes](#kw:clutter-classification-values:ce-express-geodata)**
  - Represents land use classes.
  - GeoTIFF raster format
  - Coordinate system – projected
  - Resolution (cell size) – centimeter level
  - Raster name: clutterClasses.tif

![Clutter classes raster example](../../assets/images/ce-pro/training-01/p007-img1.png)

| OBJECTID | clutter_class_name | clutter_class_id | height | nominal_distance | surface_refractivity | relative_permitivity | surface_conductivity | express_id | color | ids |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | buildings | 1 | 0 | 27 | 315 | 5 | 0.001 | 36 | #FFAF00 | 0 |
| 2 | forest | 2 | 10 | 27 | 315 | 13 | 0.004 | 36 | #23a100 | 2 |
| 3 | denseForest | 4 | 15 | 27 | 315 | 13 | 0.004 | 36 | #145C00 | <Null> |
| 4 | urban | 5 | 0 | 27 | 315 | 5 | 0.001 | 36 | #4d4d4d | 7 |
| 5 | denseUrban | 7 | 0 | 27 | 315 | 5 | 0.001 | 36 | #3B3B3B | <Null> |
| 6 | bareGround | 8 | 0 | 27 | 315 | 10 | 0.002 | 36 | #aeff21 | 11, 4 |
| 7 | crops | 9 | 2 | 27 | 315 | 20 | 0.03 | 36 | #c7ba00 | 8 |
| 8 | water | 11 | 0 | 27 | 365 | 80 | 1 | 36 | #57c7ff | 1 |
| 9 | road | <Null> | 0 | 27 | 315 | 10 | 0.002 | 36 | #3B3B3B | <Null> |

## Clutter Types

**Corine Land Cover**

![Corine Land Cover clutter class legend](../../assets/images/ce-pro/training-01/p008-img1.png)

## Raster from Vector Data

![ArcGIS Pro View ribbon — Geoprocessing pane](../../assets/images/ce-pro/training-01/p009-img1.png)

![Toolboxes pane — Conversion Tools > To Raster > Feature to Raster](../../assets/images/ce-pro/training-01/p009-img2.png)

![Feature to Raster geoprocessing tool parameters](../../assets/images/ce-pro/training-01/p009-img3.png)

Following should be defined: input layer, output raster cell size, data field that will be converted to grid, output raster file name.

*Note:* if some features in input layer are selected, only selected ones will be converted.

## Environment Settings

![Processing Extent — Extent of data in all layers dropdown](../../assets/images/ce-pro/training-01/p010-img1.png)

![Processing Extent — X and Y Extent values](../../assets/images/ce-pro/training-01/p010-img2.png)

![Raster Analysis — Cell Size and Snap Raster settings](../../assets/images/ce-pro/training-01/p010-img3.png)

![Environments — Output Coordinate System settings](../../assets/images/ce-pro/training-01/p010-img4.png)

## Raster Calculator

![Geoprocessing search for the Raster Calculator tool](../../assets/images/ce-pro/training-01/p011-img1.png)

![Raster Calculator tool building surface.tif from elevation.tif and building_height.tif](../../assets/images/ce-pro/training-01/p011-img2.png)

## Model Builder

**Automate your GIS tasks**

![ModelBuilder diagram automating the terrain and building height raster workflow](../../assets/images/ce-pro/training-01/p012-img1.png)

---