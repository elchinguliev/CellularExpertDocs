# 00. Data types

Introduction: Data types




www.cellular-expert.com
Data Types

Data can be:
1. Vector
     •   Points
     •   Lines
     •   Polygons
2. Raster
     •   GeoTIFF
3. Tabular




                    2
Modelling Outdoor coverage

The CE tools make use o
---
 three distinct GIS data layers to obtain high
precision modelling o
---
 radio wave propagation losses:
1. Digital Terrain Model (DTM), also known as Digital Elevation
   Model (DEM), which describes Earth sur
---
ace, i.e., path terrain
   pro
---
ile in terms o
---
 ground elevation above uni
---
orm sea level.
2. Obstacles layer, delineating buildings and other such objects
   above Earth sur
---
ace that may be considered to be principal
   impediments 
---
or radio wave propagation.
3. Clutter layer, delineating natural occurring or human cultivated
   ground cover that may be partially penetrable by radio waves,
   such as natural vegetation (e.g., 
---
orests, trees, bushes) or various
   crops, gardens, parks, etc.
                                Di
---

---
raction           Free Space Loss


                                                     Di
---

---
raction
                                                                        Hobstacles
                           Hclutter                                                  DSM
   Clutter losses

  UE
                                                                                       DTM




                                                                                             3
Raster Type Input: Elevation

•   Digital terrain model (DTM)
    • Represents Earth’s ground/water level above sea level
    • GeoTIFF raster 
---
ormat
    • Height values in meters
    • Coordinate system – projected
    • Resolution (cell size) – centimeter level
    • Raster name: elevation.ti
---





                                                              4
Raster Type Input: Clutter height

•   Clutter height
     • Represents objects height above elevation raster.
     • GeoTIFF raster 
---
ormat
     • Height values in meters
     • Coordinate system – projected
     • Resolution (cell size) – centimeter level
     • Raster name: clutterHeight.ti
---





                                                           5
DTM vs. Sur
---
ace


          Tx
                                  Visible
                                         Rx


                  Visible

                            Rx
                                               Sur
---
ace grid
          Tx




                                               Obstacles grid
                  Visible        Not visible
                       Rx               Rx
                                               Elevation grid

                                                                6
Clutter classes

•   Clutter classes
     • Represents land use classes.
     • GeoTIFF raster 
---
ormat
     • Coordinate system – projected
     • Resolution (cell size) – centimeter level
     • Raster name: clutterClasses.ti
---





                                                   7
Clutter types
 Corine Land Cover




                     8
Raster 
---
rom vector data




Following should be de
---
ined: input layer,
output raster cell size, data 
---
ield that will be
converted to grid, output raster 
---
ile name.
Note: i
---
 some 
---
eatures in input layer are selected,
only selected ones will be converted.


                                                      9
Environment Settings




                       10
Raster Calculator




                    11
Model Builder
Automate your GIS tasks




                          12
Questions?




www.cellular-expert.com

## Slide Images

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-000.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-001.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-002.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-003.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-004.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-005.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-006.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-007.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-008.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-009.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-010.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-011.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-012.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-013.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-014.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-015.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-016.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-017.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-018.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-019.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-020.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-021.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-022.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-023.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-024.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-025.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-026.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-027.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-028.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-029.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-030.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-031.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-032.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-033.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-034.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-035.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-036.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-037.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-038.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-039.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-040.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-041.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-042.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-043.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-044.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-045.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-046.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-047.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-048.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-049.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-050.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-051.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-052.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-053.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-054.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-055.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-056.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-057.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-058.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-059.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-060.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-061.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-062.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-063.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-064.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-065.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-066.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-067.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-068.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-069.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-070.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-071.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-072.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-073.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-074.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-075.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-076.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-077.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-078.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-079.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-080.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-081.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-082.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-083.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-084.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-085.png)

![](../../../assets/images/ce-pro/training-pdf-00-data-types/img-086.png)

