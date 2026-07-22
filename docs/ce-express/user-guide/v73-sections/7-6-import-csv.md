# 7.6 Import CSV

This tool is integrated into the “CE API” tool. It is possible to import data from .csv files. Note(!): Consult

![Image p284](../../../assets/images/ce-express/user-guide-v73/p284-img1.png)

![Image p284](../../../assets/images/ce-express/user-guide-v73/p284-img2.png)

![Image p284](../../../assets/images/ce-express/user-guide-v73/p284-img3.png)

![Image p284](../../../assets/images/ce-express/user-guide-v73/p284-img4.png)
with the administrator before import.
“Import CSV” opens a new window:

Data can be imported either as a new table (level 0), or added as a child table to a parent table (level 1).

![Image p285](../../../assets/images/ce-express/user-guide-v73/p285-img1.png)

![Image p285](../../../assets/images/ce-express/user-guide-v73/p285-img2.png)
When adding a new table, it is required to define the table name. When adding a child table to a parent
table, it is required to enter the parent table name.
Requirements:
1. The data in the CSV file should be separated by the symbol “;”
2. Avoid space and special characters in the table name
3. Level 0 table – CSV file must comprise a column object_id
4. Level 1 table – CSV file must comprise a column object_id and a column parent_id, with the
parent_id value equal to the object_id of the parent table
When adding a child table to a parent table, choose the parent table from the dropdown menu:
Partial Import

The Partial Import feature allows to add records to an already existing table. If the box "Partial import” is

![Image p286](../../../assets/images/ce-express/user-guide-v73/p286-img1.png)

![Image p286](../../../assets/images/ce-express/user-guide-v73/p286-img2.png)

![Image p286](../../../assets/images/ce-express/user-guide-v73/p286-img3.png)

![Image p286](../../../assets/images/ce-express/user-guide-v73/p286-img4.png)
checked, the new records will be added to the defined table:
