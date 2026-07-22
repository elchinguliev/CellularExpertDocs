# 3.1.28 Utilities

Click this button to open Utilities tool.
3.1.28.1 Beamwidth to HCM code
Used to generate HCM pattern codes from vertical & horizontal beamwidth values. Useful when you do not

![Image p186](../../../assets/images/ce-express/user-guide-v73/p186-img1.png)

![Image p186](../../../assets/images/ce-express/user-guide-v73/p186-img2.png)
know the exact antenna model for your cells, and only have beamwidth values assigned to them.
After uploading the CSV file you are prompted to assign the CSV fields to the required parameters:
3.1.28.2 Feature name to object ID
Used to extract feature object_id values given their names in the csv. Useful when you want to import

features with object_id references to other already existing features. E.g.: assign cell_id field to
measurements given cell_name.
3.1.28.3 Assign antennas to cells by name
Takes a .csv file with an antenna name field, and outputs the same file with antenna_id field added.
Antenna_id values are filled by finding a matching antenna in the CE Express antenna database and
assigning it’s ID to the row.
3.1.28.4 SMADEF-XML to frequency plan CSV
Pulls allotment section of SMADEF-XML file and outputs a CSV with a frequency plan carrier list, that may

![Image p187](../../../assets/images/ce-express/user-guide-v73/p187-img1.png)

![Image p187](../../../assets/images/ce-express/user-guide-v73/p187-img2.png)
be imported through the link frequency plans tool.
3.1.28.5 Export features to KMZ
Exports selected or all features to a KMZ file.
