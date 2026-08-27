# Creating Objects

## Create Object

- Import from text (done in previous exercise)
- Create manually using Add Object tool:
  - Cell
  - Site
  - Repeater
  - CPE
  - Etc.
- Duplicate existing object or objects in the project
- Move existing object or objects in the project

![Add Object tool](../../assets/images/ce-pro/training-06/p002-img1.png)

## Steps to Create Cell

- Define location
  - Type specific coordinates in:
    - Projected coordinate system – X and Y coordinates
    - Geographical coordinate system – Latitude and Longitude coordinates
  - Click on the map: coordinates will be filled automatically from point defined on the map.
- Define direction (azimuth) – this will be required if Cell object coordinates will be taken by click on the map.
- Define name
- Choose Template or fill parameters manually

![Cell Properties panel](../../assets/images/ce-pro/training-06/p003-img1.png)

![Cell placed on map](../../assets/images/ce-pro/training-06/p003-img2.png)

## Template

- Automatically fills the attributes
- Template Manager
- Own table

![Template feature classes](../../assets/images/ce-pro/training-06/p004-img3.png)

![Template dropdown](../../assets/images/ce-pro/training-06/p004-img1.png)

![Template Manager panel](../../assets/images/ce-pro/training-06/p004-img2.png)

![Cell Template Name attribute table](../../assets/images/ce-pro/training-06/p004-img4.png)

## Create Cell

**Cell** – logical information about sector: a set of channels

- RF prediction does not require Site object. Cells can be created without Site object.
- Cell still has SiteID value, which can be define in the attributes.
- SiteID is used for Carrier Aggregation.

**Site** – location point with unique identifier: Base station

- Site and Cell is connected through SiteID value.
- SiteID must be Integer.
- Site name is defined for Site object.

## Object Editor

- Open Object Editor
- Select features
- Double click on object
- Apply – to save changes
- Prediction model
- Antenna

![Object Editor panel](../../assets/images/ce-pro/training-06/p006-img1.png)

## Move / Duplicate

- Object Editor
- Select objects
- Move / Duplicate
- Select point / Define coordinates
- Save