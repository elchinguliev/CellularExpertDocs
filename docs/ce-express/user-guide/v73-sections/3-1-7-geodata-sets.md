# 3.1.7 Geodata sets

Click this button ![icon](../../../assets/images/ce-express/user-guide-v73/p084-img1.png) to open Geodata sets tool.
Geodata sets are collections of geographical raster data that is used in CE calculations. Geodata sets are
comprised of the following raster types:
Elevation – DTM (Digital terrain model), each pixel defines the absolute terrain height above sea level. No
buildings or other obstacles are included in this height.
Clutter height (optional) – Relative height of obstructions (buildings, forests, etc.) above elevation.
[Clutter classes](#kw:clutter-classification-values:ce-express-geodata) (optional) – Each pixel defines the ID of the clutter class, which the area belongs to.
Usually derived from land use data. If building heights are included in the clutter height raster, the clutter

![Image p84](../../../assets/images/ce-express/user-guide-v73/p084-img2.png)
classes raster must have building outlines separated into their own class ID.
To edit a geodata set, click the desired geodata set name from the list. To create a new one, click “+ New
geodata set”.
When creating a new geodata set, some general details, like the geodata set name, must be entered and

saved. Only then you may then upload the geodata rasters to the set after selecting it from the list.
Under the rasters section, there are 3 File upload squares for uploading the rasters. Click to select a file

![Image p85](../../../assets/images/ce-express/user-guide-v73/p085-img1.png)
or drag & drop to upload a raster file.
Uploaded rasters have the following requirements:
- Must be in projected coordinate system
- Coordinate system units must be meters
- All rasters must have the same coordinate system
- Raster resolution in X and Y axis must match
After uploading rasters, the file upload squares change to green, and show some metadata, like upload
date and resolution, about the uploaded raster files.
The data extent is also outlined in green on the map when a geodata set is selected:

3.1.7.1 [Clutter classes](#kw:clutter-classification-values:ce-express-geodata)
If a clutter class raster is available in the geodata set, the clutter classes section should be set up to
represent the data in the file.
All available clutter class raster values are listed under the “Used” and “Unused” categories.
Each relevant clutter class needs these fields filled out:
IDs in geodata raster – clutter class IDs from your uploaded clutter classes raster need to be assigned to
predefined clutter classes within CE. For example if your clutter classes raster has buildings outlined with
the ID of 2, you would need to assign “2” to the buildings clutter class in the menu. Multiple IDs may be
assigned to each class.
Height – Nominal height for clutter class if it is not represented in the clutter height raster. If you already

![Image p86](../../../assets/images/ce-express/user-guide-v73/p086-img1.png)

![Image p86](../../../assets/images/ce-express/user-guide-v73/p086-img2.png)
have heights for this class in the clutter height raster, this should be set to 0.

Color – the color by which the clutter class is represented in different UI elements, for example – the profile

![Image p87](../../../assets/images/ce-express/user-guide-v73/p087-img1.png)
chart.
