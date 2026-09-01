# Database organization

## Page setup and navigation

### Organization of single and multiple tables

The number of records displayed per page can be set on the bottom left corner. Furthermore, you may scroll through the pages using the commands in the bottom middle and bottom right corner. The table name (here: cells), the total quantity of entries (here: 20607), and the quantity of currently selected entries (here: 0) are shown on the top right corner.

![Table view with the records-per-page and paging controls highlighted](../../assets/images/inventory3d/user-guide/p012-fig1-table-recordsperpage.png)

Note that the number of filtered records will be shown, if the user applies a filter:

![Table view showing the filtered record count in the top right corner](../../assets/images/inventory3d/user-guide/p012-fig2-table-filtered.png)

### Organization of columns

The column order can be adjusted by clicking on ![icon](../../assets/images/inventory3d/user-guide/p009-icon-showselected.png) in the top right corner.

![Table view with the column organization button highlighted](../../assets/images/inventory3d/user-guide/p013-fig1-table-hamburger.png)

A menu opens in which the position of the columns can be sorted by clicking the arrow symbols. Individual columns are switched visible/invisible by clicking on the eye symbols.

![Column organization menu listing columns with visibility and order controls](../../assets/images/inventory3d/user-guide/p013-fig2-column-menu.png)

The columns can be sorted alphabetically from A>Z or from Z>A using the up and down arrow symbols within the column headers:

![Column header with the sort arrow highlighted](../../assets/images/inventory3d/user-guide/p013-fig3-table-sortarrow.png)

### Navigation across tables

There are 2 ways to change from one table to another. Either click on the table name in the top right (here: cells) and a menu opens with all available tables.

![Table name menu listing all available tables](../../assets/images/inventory3d/user-guide/p014-fig1-table-fullmenu.png)

## Filtering, sorting, editing, and linking database records

The database entries can be sorted according to their individual values. To do so, click on the column header and a dropdown menu opens with the following functions: "Set selected", "Add link", "Clear this filter", "Clear all filters", "Set defaults" and "Set as default sort field":

![Column header dropdown menu with Set selected, Add link and filter options](../../assets/images/inventory3d/user-guide/p014-fig2-dropdown-fields.png)

Alternatively, and more convenient for simple searches, columns can be filtered using the "quick filter" fields below the column names:

![Quick filter fields below the column headers](../../assets/images/inventory3d/user-guide/p015-fig1-quickfilter.png)

Users can use star symbol "\*" as wildcard. Possible filtering options:

- `*` - any non-null value
- `!*` - null value
- `[text]` - anything that contains the [text] value at the beginning. The same as `[text]*`
- `[text]*`
- `*[text]`
- `[text]*[text]`
- `![text]` - anything but the defined [text] value
- `"[text]"` - for exact match of value

Filtering options for numeric values:

- `=n` - exact match of n
- `<>n` - anything else but n
- `<n` - less than n
- `>n` - greater than n
- `<=n` - less than or equal to n
- `>=n` - greater than or equal to n

The Filter function can be used on several columns simultaneously. The headers of columns with active Filter function are marked in pink color:

![Table with several column filters active, headers marked in pink](../../assets/images/inventory3d/user-guide/p016-fig1-filtered-pink.png)

Filters can be cleared by clicking on Clear all filters.

### Set selected

This feature allows bulk editing of several records at once: Select the respective records, click on the column header and choose "Set selected" from the dropdown menu. A dialog opens with a text field. Fill in the term you want the selected database records to be changed to. Then click on "Change".

1. Select the records

   ![Records selected in the table view](../../assets/images/inventory3d/user-guide/p016-fig2-step1-select.png)

2. Click on the required column header (here: tilt) and choose Set selected

   ![Column header dropdown with Set selected highlighted](../../assets/images/inventory3d/user-guide/p016-fig3-step2-menu.png)

3. Define the new value and click Change

   ![Dialog to define the new value and confirm with Change](../../assets/images/inventory3d/user-guide/p016-fig4-step3-dialog.png)

### Add link

Each database record may comprise reference links to other database records. This means that a link can be added to reach another database record.

Select the respective record, click on the column header and choose "Add link" from the dropdown menu. In the pop up window, click on Add new reference. A list of component types opens. Select the one you want to link to. Choose the component and confirm the selection. A new link has been created.

1. Select the record

   ![Record selected in the table view](../../assets/images/inventory3d/user-guide/p017-fig1-step1-select.png)

2. Click on the required column header (here: miscloss) and choose Add link

   ![Column header dropdown with Add link highlighted](../../assets/images/inventory3d/user-guide/p017-fig2-step2-addlink.png)

3. Click on Add new reference ...

   ![Edit references dialog with Add new reference](../../assets/images/inventory3d/user-guide/p017-fig3-step3-addref.png)

4. Select the type of component you want to link to (here: calculation tasks)

   ![List of component types to link to](../../assets/images/inventory3d/user-guide/p018-fig1-step4-selecttype.png)

5. Choose the repeater(s) you want to link to and confirm the selection with ![icon](../../assets/images/inventory3d/user-guide/p018-icon-confirmselect.png) in the top left corner

   ![Repeaters list with the confirm selection button](../../assets/images/inventory3d/user-guide/p018-fig2-step5-choose.png)

6. The link has been created

   ![Table view showing the newly created link](../../assets/images/inventory3d/user-guide/p018-fig3-step6-linkcreated.png)

## Adding, viewing, downloading and deleting attachments

Each database entry can be connected with any type of attachment, for example, a picture or a text file. Entries with connected attachments have a blue check symbol next to the paper clip symbol in the column "Inc.", while entries without attachment have only the paper clip.

![Table view with the attachment indicator column highlighted](../../assets/images/inventory3d/user-guide/p019-fig1-attach-indicator.png)

**Adding attachments**

To connect a database entry with an attachment, click on the paper clip symbol in the column "Inc.". A dialog opens that allows you to browse your computer for the attachment of your choice or to take a photo.

![Select attachments or take photo dialog](../../assets/images/inventory3d/user-guide/p019-fig2-attach-dialog.png)

**Viewing, downloading and deleting attachments:**

To view the list of attachments connected to an entry, select the respective entry and click on ![icon](../../assets/images/inventory3d/user-guide/p009-icon-viewattach.png) in the toolbar:

![Toolbar with the view attachments button highlighted](../../assets/images/inventory3d/user-guide/p020-fig1-attach-icon-toolbar.png)

![Attachments dialog listing the attached files](../../assets/images/inventory3d/user-guide/p020-fig2-attachments-list.png)

In the attachments the listed images are shown as thumbs. Select an attachment from the list and it opens in a separate browser tab.

Another way to view an attachment list is to move the pointer over the check symbol in the column "Inc." and to click the right mouse button.

The selected attachments can also be downloaded.

To delete an attachment, click on the red cross symbol.

## Search (sieve)

It is possible to display only selected data from an open table. Click on the button ![icon](../../assets/images/inventory3d/user-guide/p008-icon-search.png) in the toolbar.

![Toolbar with the search (sieve) button highlighted](../../assets/images/inventory3d/user-guide/p021-fig1-search-icon-table.png)

And a dialog will open:

![Search items dialog, empty](../../assets/images/inventory3d/user-guide/p021-fig2-search-dialog-empty.png)

Note that by clicking "Add rule" you may search (sieve) with two or more filter terms that are connected via the operation "OR", not "AND". Thus, the result of two filters will show all items that comprise either the first or the second search term in their attributes.

For example, do you want to search the table cells for records starting with defined characters? Then the Search tool will help.

![Search items dialog filled in with two filter terms](../../assets/images/inventory3d/user-guide/p021-fig3-search-dialog-filled.png)

Click Add rule in order to add another search term, or click Clear all to remove all active searches.

To start the sieve process, click OK.

**Results**

![Table view showing the filtered results](../../assets/images/inventory3d/user-guide/p022-fig1-results.png)

## CE API

It is possible to call other tools configured by the administrator. For every table a different tool can be configured. To start tool selection, click on the button ![icon](../../assets/images/inventory3d/user-guide/p010-icon-ceapi.png) in the toolbar.

## Import CSV

This tool is integrated into the "CE API" tool. It is possible to import data from .csv files. Note(!): Consult with the administrator before import.

"Import CSV" opens a new window:

1. ![CSV Import dialog](../../assets/images/inventory3d/user-guide/p022-fig2-csvimport-dialog.png)

Data can be imported either as a new table (level 0), or added as a child table to a parent table (level 1). When adding a new table, it is required to define the table name. When adding a child table to a parent table, it is required to enter the parent table name.

Requirements:

1. The data in the CSV file should be separated by the symbol ";"
2. Avoid space and special characters in the table name
3. Level 0 table – CSV file must comprise a column object_id
4. Level 1 table – CSV file must comprise a column object_id and a column parent_id, with the parent_id value equal to the object_id of the parent table

When adding a child table to a parent table, choose the parent table from the dropdown menu:

2. ![CSV Import dialog with parent table name suggestions](../../assets/images/inventory3d/user-guide/p023-fig1-csv-parent-dropdown.png)

**Partial Import**

The Partial Import feature allows to add records to an already existing table. If the box "Partial import" is checked, the new records will be added to the defined table:

3. ![CSV Import dialog with Partial import checked](../../assets/images/inventory3d/user-guide/p023-fig2-partial-import.png)
