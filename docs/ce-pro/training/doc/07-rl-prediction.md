
**7. RL Introduction**

# Objective

This tutorial will show you how to add new MW links, manage and do predictions.

At the end of the exercise you will be able to:

- Create and import MW equipment.

- Create MW links in the project.

- Do MW Predictions.

# Initial data

Prepared project with:

- Network objects.

- Geodata.

- Equipment and models.

<img src="../../../assets/images/ce-pro/training-07/image1.png" style="width:6.5in;height:3.37361in" alt="A screenshot of a computer Description automatically generated" />

# Manage MW equipment

Navigate to C:\CE_Course\RL_Prediction\Project and run Project.aprx file to open the prepared project for RL Introduction exercise.

Microwave links involve additional equipment settings compared to point-to-area predictions. These settings include frequency plans, radio equipment, and parabolic antennas, which are used for predicting power budget, interference, or availability. In this section, we will cover how to create and, if necessary, import this data into the project.

## Parabolic antennas

Open Antenna Viewer in CE RLP tab, and change antenna type from Sector to Parabolic.

<img src="../../../assets/images/ce-pro/training-07/image2.png" style="width:4.17in;height:0.98in" alt="A screenshot of a computer Description automatically generated" />

All parabolic antennas will be displayed.

<img src="../../../assets/images/ce-pro/training-07/image3.png" style="width:6.5in;height:1.72708in" alt="A graph showing a line Description automatically generated with medium confidence" />

Close Antenna Viewer tool. To import a new parabolic antenna, open Import/Export Antenna Files tool. Select Parabolic (NSMA Format).

<img src="../../../assets/images/ce-pro/training-07/image4.png" style="width:4.02in;height:1.33in" alt="A screenshot of a computer Description automatically generated" />

Click on Select Antenna Model Files

<img src="../../../assets/images/ce-pro/training-07/image5.png" style="width:4.92777in;height:0.29171in" />

Browse to C:\CE_Course\RL_Prediction\Equipment, select Antenna10GHz.txt file and press OK button. It will appear in Import/Export Antenna Files dialog.

<img src="../../../assets/images/ce-pro/training-07/image6.png" style="width:4.05in;height:1.45in" alt="A screenshot of a computer Description automatically generated" />

Select Check box near the antenna and press Import Antennas button.

<img src="../../../assets/images/ce-pro/training-07/image7.png" style="width:4in;height:2.08in" alt="A screenshot of a computer Description automatically generated" />

Antenna will be imported successfully, you can go back you Antenna Viewer dialog and preview it.

<img src="../../../assets/images/ce-pro/training-07/image8.png" style="width:6.5in;height:2.29236in" alt="A screen shot of a graph Description automatically generated" />

Close Antenna Viewer and Import tools.

## Radios

This equipment category encompasses details about radio transceivers utilized in microwave links. It comprises information on transmitter power, receiver sensitivity, noise figure, nonlinearity characteristics, and maximum data capacity.

Open Radios tool in CE RLP tab and preview available Radio within default CE workspace.

<img src="../../../assets/images/ce-pro/training-07/image9.png" style="width:2.47917in;height:3.79516in" alt="A screenshot of a computer Description automatically generated" />

It has parameter section, and Modulations section.

<img src="../../../assets/images/ce-pro/training-07/image10.png" style="width:2.55208in;height:2.60452in" alt="A screenshot of a computer Description automatically generated" />

Click on Add button in top right corner of the dialog.

<img src="../../../assets/images/ce-pro/training-07/image11.png" style="width:0.36463in;height:0.28129in" />

Define the same parameters as defined below:

- Model: RL Radio

- Manufacture: CE

- Frequency From, MHz: 9500

- Frequency To, MHz: 10500

- Bandwidth, MHz: 10

- MTBF, h: 300000

- MTTR, h: 24

- Bit Rate, kbps: 2048

- Block Size, bits: 2048

- Burst Errors: 1

- Dispersive Fade Margin, dB: 50

- BER 10-3 Threshold, dBm: -76

- BER 10-6 Threshold, dBm: -72

- Noise Figure, dB: 5

- Residual BER: 1E-12

- IIP2, dBm: 30

- IIP3, dBm: 29

- XPIF, dB: 20

- Power, dBm: 20

- Power Low, dBm: 10

- Power High, dBm: 26

- Automatic Transfer Power Control Range, dB: 20

<img src="../../../assets/images/ce-pro/training-07/image12.png" style="width:2.27083in;height:4.97735in" alt="A screenshot of a computer Description automatically generated" /><img src="../../../assets/images/ce-pro/training-07/image13.png" style="width:2.73958in;height:4.94993in" alt="A screenshot of a computer Description automatically generated" />

Click on Modulations tab, and include these modulations:

<img src="../../../assets/images/ce-pro/training-07/image14.png" style="width:3.65676in;height:1.82317in" alt="A screenshot of a computer Description automatically generated" />

You can do it simply selecting modulation from the list and press + button to add it for the radio.

Each modulation has its own default parameters.

<img src="../../../assets/images/ce-pro/training-07/image15.png" style="width:2.8in;height:3.85in" alt="A screenshot of a computer Description automatically generated" />

Leave default parameters and press Create button. The new radio will be added in the list.

<img src="../../../assets/images/ce-pro/training-07/image16.png" style="width:2.91in;height:1.63in" alt="A screenshot of a computer Description automatically generated" />

Close Radios tool.

## Frequency plans

Frequency planning is important for microwave link design, optimizing spectrum use, and preventing interference. By strategically allocating frequency bands, it enhances efficiency, complies with regulations, and coordinates with other services. This planning considers propagation characteristics and facilitates scalability, ensuring optimal performance for microwave links in various environments and supporting future technology upgrades.

Frequency plans can be imported from a text file, or created manually.

### Create manually

Open Frequency Plans tool in CE RLP tab.

<img src="../../../assets/images/ce-pro/training-07/image17.png" style="width:6.5in;height:1.32431in" alt="A white screen with a black text Description automatically generated with medium confidence" />

Click on Add section and define:

- Frequency Plan Name: FP 10MHz 8 Carriers

- Low Frequency, MHz: 9800

- Carrier Spacing, MHz: 50

- Duplex Spacing, MHz: 300

- Carriers: 8

High Frequency, MHz will be filled automatically.

<img src="../../../assets/images/ce-pro/training-07/image18.png" style="width:6.5in;height:1.59861in" alt="A graph with blue bars Description automatically generated with medium confidence" />

Press Add Frequency Plan button.

The new frequency plan will appear in the main dialog.

<img src="../../../assets/images/ce-pro/training-07/image19.png" style="width:6.5in;height:1.59653in" alt="A graph with blue bars Description automatically generated with medium confidence" />

### Import

Click on Import option, and then on Select Data Files.

<img src="../../../assets/images/ce-pro/training-07/image20.png" style="width:5.02in;height:1.43in" alt="A screenshot of a computer Description automatically generated" />

Navigate to C:\CE_Course\RL_Prediction\Equipment\FrequencyPlans, select all files and press OK button.

<img src="../../../assets/images/ce-pro/training-07/image21.png" style="width:4.68in;height:4.33in" alt="A screenshot of a computer program Description automatically generated" />

Frequency Plans will be added to the preview.

<img src="../../../assets/images/ce-pro/training-07/image22.png" style="width:6.5in;height:1.60833in" alt="A graph showing a number of blue and grey bars Description automatically generated with medium confidence" />

Press Import button and they will be imported to the database.

<img src="../../../assets/images/ce-pro/training-07/image23.png" style="width:6.5in;height:1.60556in" alt="A graph of blue and black vertical lines Description automatically generated with medium confidence" />

Close Frequency Plans dialog.

# Add Links

The link objects can be imported or created manually using Add functionality. Open Add Object tool and select Link option from drop-down menu list.

<img src="../../../assets/images/ce-pro/training-07/image24.png" style="width:3.36505in;height:2.0107in" alt="A screenshot of a computer Description automatically generated" />

Click once on T1 site and second time to D1 site.

It will fill general parameters automatically.

<img src="../../../assets/images/ce-pro/training-07/image25.png" style="width:6.5in;height:4.10417in" />

Height, azimuth and other parameters are calculated automatically, leave them as it is.

Define parameters are defined below:

- Name: MW001

- Radio Model: 2. RL Radio

<img src="../../../assets/images/ce-pro/training-07/image26.png" style="width:4.18808in;height:0.84387in" alt="A screenshot of a computer Description automatically generated" />

- Frequency Plan: FP 10MHz 8 Carriers

<img src="../../../assets/images/ce-pro/training-07/image27.png" style="width:4.02139in;height:1.69815in" alt="A screenshot of a computer Description automatically generated" />

- Carriers: 1 and 3 (1’ and 3’ will be automatically assigned).

<img src="../../../assets/images/ce-pro/training-07/image28.png" style="width:3.21in;height:1.28in" alt="A screenshot of a computer Description automatically generated" />

- Go to Antenna section and change antenna to Antenna 10MHz

<img src="../../../assets/images/ce-pro/training-07/image29.png" style="width:3.49in;height:3.34in" alt="A screenshot of a computer Description automatically generated" />

Press Save Changes button.

Do not close the dialog, create new links and define parameters:

- Between D1 and E2

  - Name: MW002

  - SiteA: Lower

> <img src="../../../assets/images/ce-pro/training-07/image30.png" style="width:4.06307in;height:0.37505in" />

- Carriers: 2 and 4

> <img src="../../../assets/images/ce-pro/training-07/image31.png" style="width:3.94847in;height:1.52105in" alt="A screenshot of a computer Description automatically generated" />

- Leave other parameters as it is.

Press Save Changes

- Between E6 and M77

  - Name: MW003

  - SiteA: Lower

> <img src="../../../assets/images/ce-pro/training-07/image30.png" style="width:4.06307in;height:0.37505in" />

- Carriers: 1 and 4

> <img src="../../../assets/images/ce-pro/training-07/image32.png" style="width:4.04223in;height:1.6669in" alt="A screenshot of a computer Description automatically generated" />

- Leave other parameters as it is.

Press Save Changes

<img src="../../../assets/images/ce-pro/training-07/image33.png" style="width:6.5in;height:3.63472in" alt="A screenshot of a computer screen Description automatically generated" />

# RL Predictions

The predictions are working between selected links and provides all necessary information about power budget, interference or availability.

Select all links on the map and open Link Prediction tool. Before launching the predictions, enable Calculate Interference option.

<img src="../../../assets/images/ce-pro/training-07/image34.png" style="width:5.08in;height:3.08in" alt="A screenshot of a computer Description automatically generated" />

Press Run button and wait will prediction are completed and results loaded into your project.

<img src="../../../assets/images/ce-pro/training-07/image35.png" style="width:6.5in;height:3.38542in" alt="A screenshot of a computer Description automatically generated" />

The primary results are Power Budget and Profile between Tx and Rx. On the left, select another link and results will be updated accordingly.

<img src="../../../assets/images/ce-pro/training-07/image36.png" style="width:6.5in;height:1.33472in" alt="A screen shot of a computer Description automatically generated" />

Selected Link can have several carriers, to preview the results expand Carrier option.

<img src="../../../assets/images/ce-pro/training-07/image37.png" style="width:2.7608in;height:1.08348in" alt="A screenshot of a computer Description automatically generated" />

Click on Interference tab to display interfering links and interfered links information.

<img src="../../../assets/images/ce-pro/training-07/image38.png" style="width:6.5in;height:1.31319in" alt="A screenshot of a computer Description automatically generated" />

Total Interference is shown in Power Budget section.

<img src="../../../assets/images/ce-pro/training-07/image39.png" style="width:2.08in;height:4.11in" alt="A screenshot of a computer Description automatically generated" />

Interference link predictions can be previewed too. Click on Interfering Link in top left corner and it will display selected interfering link Power Budget, Path Loss and draw a line on the map.

<img src="../../../assets/images/ce-pro/training-07/image40.png" style="width:6.5in;height:3.37569in" alt="A screenshot of a computer Description automatically generated" />

Go back to Links section, sekect MW003 from M77 to E6.

<img src="../../../assets/images/ce-pro/training-07/image41.png" style="width:2.67746in;height:1.95861in" alt="A screenshot of a computer Description automatically generated" />

It has carrier 1’ where interference comes from MW001 Site T1:

- Interference, dBm: -181.6 dBm

- FML, dB: 2.36E 10-8

<img src="../../../assets/images/ce-pro/training-07/image42.png" style="width:6.5in;height:0.32153in" />

Close Link Prediction results, select MW001 link on the map and open Object Editor. Double click on the link.

<img src="../../../assets/images/ce-pro/training-07/image43.png" style="width:4.38603in;height:1.79192in" alt="A screenshot of a computer Description automatically generated" />

Find Frequency Plan table, select Upper and change carrier 1’ polarization to Vertical.

<img src="../../../assets/images/ce-pro/training-07/image44.png" style="width:4.45896in;height:1.54188in" alt="A screenshot of a computer Description automatically generated" />

Save Changes.

Select all links on the map, open Link Prediction tool again and run predictions.

After predictions are done, open MW003 (B-A) interference predictions and preview how Interference From is changed for MW001 link, Site S1.
