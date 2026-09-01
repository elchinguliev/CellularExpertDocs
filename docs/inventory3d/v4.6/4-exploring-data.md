# Exploring data

## Export selected

Data subsets can be exported as .xls or .csv files. Select the database records of choice, then click Export Selected ![icon](../../assets/images/inventory3d/user-guide/p010-icon-exportsel.png) button:

A pop up window opens.

![Export popup with links to download in xls or csv format](../../assets/images/inventory3d/user-guide/p023-fig3-export-popup.png)

Click on the links to choose between .xls or .csv file formats.

Note that hidden columns are not exported.

## PDF report

A PDF report summarizes information associated with one or more objects. For generating a report, first select the objects of choice. Then open the Import Export menu with ![icon](../../assets/images/inventory3d/user-guide/p011-icon-additionaltools.png) and choose "Generate report as PDF":

![Import Export menu with Generate report as PDF highlighted](../../assets/images/inventory3d/user-guide/p024-fig1-importexport-menu.png)

A new dialog appears. Open the PDF report by clicking to the file name:

![Export complete dialog with a link to the generated PDF report](../../assets/images/inventory3d/user-guide/p024-fig2-export-complete.png)

Note that the administrator has to prepare the template for the PDF report. Please inform the administrator in case of problems with generating PDF reports.

## File browser

Open the Data Export menu with ![icon](../../assets/images/inventory3d/user-guide/p011-icon-additionaltools.png) and choose "File Browser":

![Import Export menu with File Browser highlighted](../../assets/images/inventory3d/user-guide/p025-fig1-filebrowser-menu.png)

View attached files, download or delete files:

![File browser tree showing folders and attached files](../../assets/images/inventory3d/user-guide/p025-fig2-filebrowser-tree.png)

Images are shown as thumbs. Note that it is possible to rotate the images.

**File Browser Toolbar:**

![icon](../../assets/images/inventory3d/user-guide/p025-icon-dataviewpanel.png) Open the Data View Panel

![icon](../../assets/images/inventory3d/user-guide/p026-icon-goback.png) Go one step back

![icon](../../assets/images/inventory3d/user-guide/p026-icon-selectallfiles.png) Select / unselect all files and folders

![icon](../../assets/images/inventory3d/user-guide/p026-icon-downloadfiles.png) Download selected files

![icon](../../assets/images/inventory3d/user-guide/p026-icon-deletefiles.png) Delete selected files

![icon](../../assets/images/inventory3d/user-guide/p026-icon-restorefiles.png) Restore selected files

When an image is deleted, said image is marked as strikethrough on the File Server:

![File browser tree with a deleted file shown as strikethrough](../../assets/images/inventory3d/user-guide/p026-fig1-strikethrough.png)

You can restore the image by selecting the strikethrough object and clicking ![icon](../../assets/images/inventory3d/user-guide/p026-icon-restorefiles.png):

![File browser tree with the restored file selected](../../assets/images/inventory3d/user-guide/p027-fig1-restore.png)

## Quick references

Quick references are defined by the administrator and allow users to open a reference object in a separate browser tab. If Quick references are enabled, the respective column is marked with "\*", for example "site":

![Table view with the site column marked with an asterisk for quick references](../../assets/images/inventory3d/user-guide/p027-fig2-quickref-table.png)

To open a reference link, select it in edit mode (right click on it) and click "here" in the opened dialog.

![Dialog with a link to open the referenced element](../../assets/images/inventory3d/user-guide/p028-fig1-referenced-popup.png)

The referenced object is opened in a separate browser tab.

## Default editing and manual editing

If the administrator has defined default values (Administrator Guide: "Set Defaults"), editing column information may include selecting values from a drop-down menu. If the menu does not comprise the desired value, users may manually edit the information or clear the value:

![Column edit dropdown with Manual entry and Clear value options](../../assets/images/inventory3d/user-guide/p028-fig2-defaultedit-dropdown.png)

## External Links

It is possible to add links to external webpages to the webapp, for example:

![Table with a description column containing an external link](../../assets/images/inventory3d/user-guide/p028-fig3-externallink-example.png)

## Displaying Rasters

It is possible to display raster type of data, similar to graphical layers, on the map. Rasters are created by the administrator, but users may also access and configure the table map_rasters:

![map_rasters table](../../assets/images/inventory3d/user-guide/p028-fig4-maprasters-table.png)

If the raster is a PNG or JPG file, users can edit the coordinates of the top-left and bottom-right corners of the picture in the columns West, East, North, and South, and define the opacity.

Example raster:

![Example raster displayed on the map](../../assets/images/inventory3d/user-guide/p029-fig1-example-raster.png)

**Raster legend**

From the table map_rasters users may access and configure the child table map_rasters_legend, in which the raster legend is defined:

![map_raster_legend table with color and label fields](../../assets/images/inventory3d/user-guide/p029-fig2-rasterlegend-table.png)

The legend color is defined in the field Color. The field must comprise the color code which is formatted as follows: `#RRGGBB`, where RR is red color value in hexadecimal format, GG is green color value in hexadecimal format, and BB is blue color value in hexadecimal format. For example, code `#00FF00` would mean green color. The color value can be acquired from the picture using any software with a color picking tool, e.g. Microsoft Paint or Free Color Picker.

The legend labels are defined in the field Label of the table "map_raster_legend".

Rasters and Raster legends are shown in the list Layers.

![Map with the raster legend shown in the Layers list](../../assets/images/inventory3d/user-guide/p030-fig1-raster-legend-onmap.png)
