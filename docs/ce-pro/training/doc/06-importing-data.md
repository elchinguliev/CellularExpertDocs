
**6. Importing data**

# Objective

This tutorial will show you how to import network objects using different data structures to Cellular Expert workspace.

At the end of exercise you will be able to:

- Create Json mapping file.

- Import objects.

# Initial data

Prepared project with:

- Geodata.

# Excel/CSV file

Navigate to C:\CE_Course\ImportingData\Project location and run Project.aprx to open the prepared project for this exercise.

Right-click on Cells layer in Contents window and choose Attribute Table, preview table structure, and fields.

<img src="../../../assets/images/ce-pro/training-06/image1.png" style="width:6.5in;height:0.40625in" />

Click on Table Options button and select Field View.

<img src="../../../assets/images/ce-pro/training-06/image20.png" style="width:3.09108in;height:1.72917in" />

It will provide more detailed information about table structure.

<img src="../../../assets/images/ce-pro/training-06/image3.png" style="width:6.5in;height:1.82708in" alt="A screenshot of a computer Description automatically generated" />

Close tables.

# Mapping file

An Excel or CSV file can be imported directly into the CE workspace without a mapping file, provided that the text file has the same field names as the Cells table in the CE workspace.

The Excel/CSV file might contain discrepancies in names, values, and units compared to the Cellular Expert database. To tackle these conflicts, an extra Mapping file is recommended to address these discrepancies.

If the import file aligns perfectly with the Cellular Expert database, a Mapping file isn't needed. However, when there are disparities, using mapping files becomes essential for a successful import. Here is a structure of one field in a mapping file.

<img src="../../../assets/images/ce-pro/training-06/image4.png" style="width:3.55258in;height:0.69801in" alt="A close-up of a clock Description automatically generated" />

**“current_name”** - name of the value that is written in the data file. As an example “freq_mhz” is a column name in the data file and will be changed to “frequency” when the mapping file is applied and objects are imported.

**“destination_name”** - the proper name of the property (table column name) in the Cellular

**“default_value”** – The default value applies when an object in the data file lacks a specific property. The same value will be applied for all imported objects.

On your computer, navigate to C:\CE_Course\ImportingData\Network and open the cells_mapping.json file. Review the contents of the file. Then, from the same Network folder, open the Cells.csv file and review it as well. Keep both files open. Your next step is to create a mapping file that will be used during the import process.

Define values in the mapping file based on this table:

|         **current_name**          | **destination_name** | **default_value** |
|:---------------------------------:|---------------------:|------------------:|
|             cell_name             |            Cell Name |     *Leave empty* |
|             latitude              |             latitude |     *Leave empty* |
|             longitude             |            longitude |     *Leave empty* |
|              height               |  Height Above Ground |     *Leave empty* |
|              azimuth              |              Azimuth |     *Leave empty* |
|               tilt                |                 Tilt |     *Leave empty* |
|             frequency             |            Frequency |     *Leave empty* |
|               power               |           Cell Power |     *Leave empty* |
|             misc_loss             |        *Leave empty* |     *Leave empty* |
|               eirp                |        *Leave empty* |     *Leave empty* |
|             bandwidth             |            Bandwidth |     *Leave empty* |
|           noise_figure            |        *Leave empty* |                 6 |
|      downlink_duplex_factor       |        *Leave empty* |               0.6 |
|        subcarrier_spacing         |        *Leave empty* |                30 |
|              tx_mimo              |               TxMIMO |     *Leave empty* |
|              rx_mimo              |               RxMIMO |     *Leave empty* |
|       active_antenna_effect       |        *Leave empty* |                 0 |
|             cell_load             |        *Leave empty* |                30 |
|           network_name            |        *Leave empty* |     *Leave empty* |
|            color_index            |        *Leave empty* |     *Leave empty* |
|            technology             |                 Tech |     *Leave empty* |
|        prediction_model_id        |        *Leave empty* |                 3 |
| prediction_model_configuration_id |        *Leave empty* |                 4 |
|          frequency_group          |            Frequency |     *Leave empty* |
|            antenna_id             |        *Leave empty* |               514 |
|             carriers              |        *Leave empty* |              \[\] |
|          electrical_tilt          |        *Leave empty* |     *Leave empty* |
|              site_id              |           Tower Name |     *Leave empty* |

<img src="../../../assets/images/ce-pro/training-06/image5.png" style="width:2.88542in;height:4.99599in" alt="A screenshot of a computer Description automatically generated" /> <img src="../../../assets/images/ce-pro/training-06/image6.png" style="width:3.02847in;height:4.94444in" alt="A screenshot of a computer program Description automatically generated" />

When the fields are filled, save the .json file. Close json and excel files.

# Importing

In CE RCP toolbar open *Import Objects from Files* <img src="../../../assets/images/ce-pro/training-06/image7.png" style="width:0.42529in;height:0.35606in" alt="A blue and white logo Description automatically generated" /> *.* Choose Import Cells from the dropdown menu.

<img src="../../../assets/images/ce-pro/training-06/image8.png" style="width:3.81in;height:1.23in" alt="A screenshot of a computer Description automatically generated" />

Choose *5G 3500 Band n48* template. Values from this template will be taken during the import process, if mapping_file would be missing some parameters.

<img src="../../../assets/images/ce-pro/training-06/image9.png" style="width:3.87in;height:1.82in" alt="A screenshot of a computer Description automatically generated" />

Click Select Data Files button.

<img src="../../../assets/images/ce-pro/training-06/image10.png" style="width:4.62565in;height:0.42714in" />

Navigate to *C:\CE_Course\ImportingData\Network.* Switch from Microsoft Excel files to Comma-separated value files (.csv).

<img src="../../../assets/images/ce-pro/training-06/image11.png" style="width:2.46909in;height:1.18767in" alt="A screenshot of a computer Description automatically generated" />

Select Cells CSV file and click OK.

<img src="../../../assets/images/ce-pro/training-06/image12.png" style="width:5.61in;height:1.14in" alt="A screenshot of a computer Description automatically generated" />

View the imported data fields. The column names should be the same as in the .csv file.

<img src="../../../assets/images/ce-pro/training-06/image13.png" style="width:3.92in;height:3.34in" alt="A screenshot of a data Description automatically generated" />

Click Select Mapping File button.

<img src="../../../assets/images/ce-pro/training-06/image14.png" style="width:5.15697in;height:0.50007in" />

Navigate to *C:\CE_Course\ImportingData\Network.* Select cells_mapping JSON file and click OK.

Click Yes in the Information window.

<img src="../../../assets/images/ce-pro/training-06/image15.png" style="width:3.2in;height:1.23in" alt="A screenshot of a computer error Description automatically generated" />

Press Import Cells button.

<img src="../../../assets/images/ce-pro/training-06/image16.png" style="width:6.5in;height:0.40694in" />

All imported cells and sites should appear on the map.

<img src="../../../assets/images/ce-pro/training-06/image17.png" style="width:6.5in;height:3.54653in" />

# Antennas

Navigate to C:\CE_Course\ImportingData\Antenna. Open ADU4518R6v06_2655.txt antenna file with Notepad.

<img src="../../../assets/images/ce-pro/training-06/image18.png" style="width:2.47in;height:2.98in" alt="A screenshot of a computer Description automatically generated" />

The antenna pattern file is in Planet format and its structure:

- General information.

- HORIZONTAL patterns.

- VERTICAL patterns.

Such kind of antenna pattern format can be imported into Cellular Expert database.

Open Import/Export Antenna Files tool. Then click on Select Antenna Model Files

<img src="../../../assets/images/ce-pro/training-06/image19.png" style="width:4.41in;height:1.37in" alt="A screenshot of a computer Description automatically generated" />

Navigate to C:\CE_Course\ImportingData\Antenna, select ADU4518R6v06_2655.txt file and press Open. It will be added to the import tool.

<img src="../../../assets/images/ce-pro/training-06/image20.png" style="width:4.38in;height:1.48in" alt="A screenshot of a computer Description automatically generated" />

Press Import Antennas button. After that you will get the message, that the antenna was imported successfully.

<img src="../../../assets/images/ce-pro/training-06/image21.png" style="width:4.48in;height:0.62in" alt="A screen shot of a computer Description automatically generated" />

Close this tool, then open Antenna Viewer tool, using the scroll bar go to the bottom and double click on the imported antenna.

<img src="../../../assets/images/ce-pro/training-06/image22.png" style="width:6.5in;height:1.50833in" alt="A screenshot of a computer screen Description automatically generated" />

# Cell import with minimum required information

Minimum required data to import Cell object is:

- Name;

- Latitude;

- Longitude.

<img src="../../../assets/images/ce-pro/training-06/image23.png" style="width:2.39617in;height:0.76052in" alt="A screenshot of a computer Description automatically generated" />

Navigate to C:\CE_Course\ImportingData\Network and open Cells_small.csv file to preview it. Also, open cells_mapping_small.json file to preview the parameters and default values, which would be applied to this cell object.

<img src="../../../assets/images/ce-pro/training-06/image24.png" style="width:2.7in;height:3.48in" alt="A screenshot of a computer program Description automatically generated" />

Close csv and json files.

Refresh Import tool, choose Import Sites.

<img src="../../../assets/images/ce-pro/training-06/image25.png" style="width:4.78192in;height:1.17725in" alt="A screenshot of a computer Description automatically generated" />

Then go back to Import Cells.

Define template: 5G 3500 Band n48 is set.

<img src="../../../assets/images/ce-pro/training-06/image26.png" style="width:4.87568in;height:1.08348in" alt="A screenshot of a computer Description automatically generated" />

Click on Select Data Files button.

<img src="../../../assets/images/ce-pro/training-06/image27.png" style="width:4.78192in;height:0.3438in" />

Switch from Microsoft Excel files to Comma-separated value files (.csv).

<img src="../../../assets/images/ce-pro/training-06/image11.png" style="width:2.46909in;height:1.18767in" alt="A screenshot of a computer Description automatically generated" />

Select Cells_small.csv file and press OK to add it.

<img src="../../../assets/images/ce-pro/training-06/image28.png" style="width:3.9in;height:0.98in" alt="A screenshot of a computer Description automatically generated" />

Click on Select Mapping file and define mapping_cells_small.json file.

<img src="../../../assets/images/ce-pro/training-06/image29.png" style="width:4.87568in;height:1.36477in" alt="A screenshot of a computer Description automatically generated" />

Press Import Cells button. New objects will be imported into the northern region.

<img src="../../../assets/images/ce-pro/training-06/image30.png" style="width:4.24017in;height:1.46895in" alt="A map of a city Description automatically generated" />
