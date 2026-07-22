# Database Organization



## 7.1 Page setup and navigation



### 7.1.1 Organization of single and multiple tables

![Image p274](../../../assets/images/ce-express/user-guide-v73/p274-img1.png)

The number of records displayed per page can be set on the bottom left corner. Furthermore, you may
scroll through the pages using the commands in the bottom middle and bottom right corner. The table name
(here: cells), the total quantity of entries (here: 20607), and the quantity of currently selected entries (here:
0) are shown on the top right corner. Note that the number of filtered records will be shown, if the user
applies a filter:

![Image p274](../../../assets/images/ce-express/user-guide-v73/p274-img3.png)

### 7.1.2 Organization of columns

The column order can be adjusted by clicking on ![icon](../../../assets/images/ce-express/user-guide-v73/p274-img5.png) in the top right corner.

![Image p275](../../../assets/images/ce-express/user-guide-v73/p275-img1.png)

A menu opens in which the position of the columns can be sorted by clicking the arrow symbols. Individual
columns are switched visible/invisible by clicking on the eye symbols.

![Image p275](../../../assets/images/ce-express/user-guide-v73/p275-img3.png)

The columns can be sorted alphabetically from A>Z or from Z>A using the up and down arrow symbols
within the column headers:

![Image p275](../../../assets/images/ce-express/user-guide-v73/p275-img4.png)

### 7.1.3 Navigation across tables

There are 2 ways to change from one table to another. Either click on the table name in the top right (here:
cells) and a menu opens with all available tables.

![Image p276](../../../assets/images/ce-express/user-guide-v73/p276-img1.png)

## 7.2 Filtering, sorting, editing, and linking database records

The database entries can be sorted according to their individual values. To do so, click on the column
header and a dropdown menu opens with the following functions: “Set selected”, “Add link”, ”Clear this
filter”, “Clear all filters”, “Set defaults” and “Set as default sort field”:

![Image p276](../../../assets/images/ce-express/user-guide-v73/p276-img2.png)

Alternatively, and more convenient for simple searches, columns can be filtered using the “quick filter” fields
below the column names:

![Image p277](../../../assets/images/ce-express/user-guide-v73/p277-img1.png)

Users can use star symbol “*” as wildcard. Possible filtering options:
*- any non-null value
!* - null value
[text] - anything that contains the [text] value at the beginning. The same as [text]*
[text]*
*[text]
[text]*[text]
![text] - anything but the defined [text] value
”[text]” - for exact match of value
Filtering options for numeric values:
=n - exact match of n
<>n - anything else but n
<n - less than n
>n - greater than n
<=n - less than or equal to n
>=n - greater than or equal to n
The Filter function can be used on several columns simultaneously. The headers of columns with active
Filter function are marked in pink color:

![Image p278](../../../assets/images/ce-express/user-guide-v73/p278-img1.png)

Filters can be cleared by clicking on Clear all filters.

### 7.2.1 Set selected

This feature allows bulk editing of several records at once: Select the respective records, click on the column
header and choose “Set selected” from the dropdown menu. A dialog opens with a text field. Fill in the term
you want the selected database records to be changed to. Then click on “Change”. Synchronize the edited
records with the database using the Synchronize changes Tool.

1. Select the records

![Image p278](../../../assets/images/ce-express/user-guide-v73/p278-img2.png)

2. Click on the required column header (here:tilt) and choose Set selected

![Image p278](../../../assets/images/ce-express/user-guide-v73/p278-img3.png)

3. Define the new value and click Change

![Image p279](../../../assets/images/ce-express/user-guide-v73/p279-img1.png)

### 7.2.2 Add link

Each database record may comprise reference links to other database records. This means that a link can
be added to reach another database record.

Select the respective record, click on the column header and choose “Add link” from the dropdown menu.
In the pop up window, click on Add new reference. A list of component types opens. Select the one you
want to link to. Choose the component and confirm the selection. A new link has been created.

1. Select the record

![Image p279](../../../assets/images/ce-express/user-guide-v73/p279-img2.png)

2. Click on the required column header (here:miscloss) and choose Add link

![Image p279](../../../assets/images/ce-express/user-guide-v73/p279-img3.png)

3. Click on Add new reference ...

![Image p280](../../../assets/images/ce-express/user-guide-v73/p280-img1.png)

4. Select the type of component you want to link to (here: calculation tasks)

![Image p280](../../../assets/images/ce-express/user-guide-v73/p280-img2.png)

5. Choose the repeaters(s) you want to link to and confirm the selection with ![icon](../../../assets/images/ce-express/user-guide-v73/p280-img5.png) in
the top left corner

![Image p280](../../../assets/images/ce-express/user-guide-v73/p280-img3.png)

6. The link has been created

![Image p280](../../../assets/images/ce-express/user-guide-v73/p280-img4.png)

## 7.3 Adding, viewing, downloading and deleting attachments

Each database entry can be connected with any type of attachment, for example, a picture or a text file.
Entries with connected attachments have a blue check symbol next to the paper clip symbol in the column
“Inc.”, while entries without attachment have only the paper clip.

![Image p281](../../../assets/images/ce-express/user-guide-v73/p281-img1.png)

**Adding attachments**

To connect a database entry with an attachment, click on the paper clip symbol in the column “Inc.”. A
dialog opens that allows you to browse your computer for the attachment of your choice or to take a photo.

![Image p282](../../../assets/images/ce-express/user-guide-v73/p282-img1.png)

**Viewing, downloading and deleting attachments:**

To view the list of attachments connected to an entry, select the respective entry and click on ![icon](../../../assets/images/ce-express/user-guide-v73/p282-img2.png) in the
toolbar:

![Image p282](../../../assets/images/ce-express/user-guide-v73/p282-img3.png)

![Image p282](../../../assets/images/ce-express/user-guide-v73/p282-img4.png)

In the attachments the listed images are shown as thumbs. Select an attachment from the list and it opens
in a separate browser tab.

Another way to view an attachment list is to move the pointer over the check symbol in the column “Inc.”
and to click the right mouse button.
The selected attachments can also be downloaded.
To delete an attachment click on the red cross symbol.

## 7.4 Sieve

It is possible to display only selected data from an open table. Click on the button ![icon](../../../assets/images/ce-express/user-guide-v73/p283-img1.png) in the toolbar.

![Image p283](../../../assets/images/ce-express/user-guide-v73/p283-img3.png)

And a dialog will open:

![Image p283](../../../assets/images/ce-express/user-guide-v73/p283-img4.png)

Note that by clicking “Add rule” you may sieve with two or more filter terms that are connected via the
operation “OR”, not “AND”. Thus, the result of two filters will show all items that comprise either the first or
the second search term in their attributes.
For example, do you want to sieve the table asites for records starting with defined characters? Then the
Sieve tool will help.

![Image p284](../../../assets/images/ce-express/user-guide-v73/p284-img1.png)

Click Add rule in order to add another search term, or click Clear all to remove all active searches.
To start the sieve process, click OK.

**Results**

![Image p284](../../../assets/images/ce-express/user-guide-v73/p284-img2.png)

## 7.5 CE API

It is possible to call other tools configured by the administrator. For every table a different tool can be
configured. To start tool selection, click on the button ![icon](../../../assets/images/ce-express/user-guide-v73/p284-img3.png) in the toolbar.

## 7.6 Import CSV

This tool is integrated into the “CE API” tool. It is possible to import data from .csv files. Note(!): Consult
with the administrator before import.

“Import CSV” opens a new window:

![Image p285](../../../assets/images/ce-express/user-guide-v73/p285-img1.png)

Data can be imported either as a new table (level 0), or added as a child table to a parent table (level 1).
When adding a new table, it is required to define the table name. When adding a child table to a parent
table, it is required to enter the parent table name.

Requirements:
1. The data in the CSV file should be separated by the symbol “;”
2. Avoid space and special characters in the table name
3. Level 0 table – CSV file must comprise a column object_id
4. Level 1 table – CSV file must comprise a column object_id and a column parent_id, with the
parent_id value equal to the object_id of the parent table

When adding a child table to a parent table, choose the parent table from the dropdown menu:

![Image p285](../../../assets/images/ce-express/user-guide-v73/p285-img2.png)

**Partial Import**

The Partial Import feature allows to add records to an already existing table. If the box "Partial import” is
checked, the new records will be added to the defined table:

![Image p286](../../../assets/images/ce-express/user-guide-v73/p286-img1.png)
