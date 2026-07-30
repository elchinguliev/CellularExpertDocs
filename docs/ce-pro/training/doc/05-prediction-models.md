**Cellular Expert**

**5. Prediction Models Exercise**

**\**

# Objective

Do calculations with different prediction models and analyze their differences.

At the end of exercise, you will be able to:

- Create prediction model.

- Change predictions model.

- Get familiar with prediction model parameters.

# Initial data

Prepared project with:

- Network objects.

- Geodata.

- Equipment and models.

<img src="../../../assets/images/ce-pro/training-05/image1.png" style="width:6.5in;height:3.3875in" alt="A screenshot of a map Description automatically generated" />

# CEC ITU-R Model (100MHz – 6GHz)

Open a project from C:\CE_Course\PredictionModels\Project location.

Open Prediction Model Manager tool and preview each Default prediction model. These models will be automatically created with new workspace.

<img src="../../../assets/images/ce-pro/training-05/image33.png" style="width:6.16495in;height:0.95833in" />

<img src="../../../assets/images/ce-pro/training-05/image2.png" style="width:2.2in;height:2.27in" alt="A screenshot of a computer Description automatically generated" />

Find cells by cell name attribute on the map:

- NBa 01

- NBa 02

- NBa 03

<img src="../../../assets/images/ce-pro/training-05/image3.png" style="width:2.625in;height:2.33129in" alt="A map of a city Description automatically generated" />

Select these cells and open Object Editor tool. Double click on first cell to open its attribute, then scroll down in parameters option to find Prediction model parameter.

<img src="../../../assets/images/ce-pro/training-05/image4.png" style="width:4.83in;height:2.62in" alt="A screenshot of a computer Description automatically generated" />

The heading shows which type and model is applied for the cell.

<img src="../../../assets/images/ce-pro/training-05/image5.png" style="width:4.9in;height:0.58in" />

Preview other cells’ prediction model. Then open Prediction Model Manager tool again and find this model there.

Double click to open it attributes.

<img src="../../../assets/images/ce-pro/training-05/image6.png" style="width:2.71in;height:7.09in" alt="A screenshot of a computer Description automatically generated" />

Then open RF Prediction tool and run the calculations with defined parameters in the picture below.

<img src="../../../assets/images/ce-pro/training-05/image7.png" style="width:4.86in;height:2.82in" alt="A screenshot of a computer Description automatically generated" />

After successful calculation, preview the results.

<img src="../../../assets/images/ce-pro/training-05/image8.png" style="width:6.5in;height:3.40486in" alt="A screenshot of a computer screen Description automatically generated" />

If prediction model provides too optimistical output to all conditions: LOS, OLOS and NLOS, then open ***3km radius*** prediction model parameters and change Offset coefficient, dB from 32 to 45. It simply works as a offset in Field Strength calculations, and would add additional 13dB loss (45 – 32 = 13 dB).

<img src="../../../assets/images/ce-pro/training-05/image9.png" style="width:3.24003in;height:0.50007in" />

Press Apply button. Run RF Predictions with the same parameters.

Leave enabled only Field Strength 1 layers from both predictions.

<img src="../../../assets/images/ce-pro/training-05/image10.png" style="width:2.09in;height:3.8in" alt="A screenshot of a computer Description automatically generated" />

Click on Map \> Explore, and then click once on the map. The tool will provide information about raster values on this location.

<img src="../../../assets/images/ce-pro/training-05/image11.png" style="width:6.04251in;height:1.10432in" alt="A screenshot of a computer Description automatically generated" />

Field Strength for second prediction is lower by 13 (because we defined higher Offset value by 13).

If Path Loss should slope higher or slower depend on distance, we can adjust two parameters:

- Distance coefficient – it affects only Line of Sight areas.

- Distance coefficient obstructed – it affects only NLOS and OLOS areas.

There is possibility to define different slope coeficients how radio wave would slope when it goes through obstacle. Change Distance coefiecient obstructed value from 40 to 30.

<img src="../../../assets/images/ce-pro/training-05/image12.png" style="width:3.15669in;height:0.39589in" />

Press Apply and RF run predictions again. Compare the predictions using Explore tool. It gives higher effect in higher distance from Cell location. So signal value provides higher signal near transmitter.

<img src="../../../assets/images/ce-pro/training-05/image13.png" style="width:1.60439in;height:0.81261in" alt="A screenshot of a computer Description automatically generated" />

And lower signal after 1km.

<img src="../../../assets/images/ce-pro/training-05/image14.png" style="width:1.04181in;height:0.77094in" alt="A screenshot of a computer Description automatically generated" />

Open 3km radius prediction model parameters again, and change other parameters:

- Frequency coefficient: from 20 to 15

- Receiver height: from 1.5 to 10

## Clutter

Open the Clutter Classes tool to preview the available clutter types. These represent the default clutter categories within the project. Here, you should map your clutter classes raster and define ID values for each clutter class. If multiple clutter classes apply, separate them with a comma.

<img src="../../../assets/images/ce-pro/training-05/image15.png" style="width:4.97986in;height:0.41672in" />

For this project, we use the Sentinel-2 land raster, with its clutter types mapped in the Clutter Classes dialog. Below is the clutter classes raster table:

<img src="../../../assets/images/ce-pro/training-05/image16.png" style="width:1.40645in;height:2.57328in" alt="A screenshot of a computer Description automatically generated" />

Value 2 corresponds to the *Trees* class and is assigned as *Forest*.

<img src="../../../assets/images/ce-pro/training-05/image17.png" style="width:4.2in;height:2.93in" />

Clutter classes has additional information – buildings.

<img src="../../../assets/images/ce-pro/training-05/image18.png" style="width:6.5in;height:1.86458in" />

That can be added separately to each clutter class raster, and buildings data ID value applied in Clutter Classes dialog.

<img src="../../../assets/images/ce-pro/training-05/image19.png" style="width:4.14in;height:2.88in" />

This is done already, preview this data.

Open 3km radius prediction model and double click on Buildings clutter class.

<img src="../../../assets/images/ce-pro/training-05/image20.png" style="width:2.32292in;height:3.98582in" alt="A screenshot of a computer Description automatically generated" />

It provides additional parameters for how the prediction model behaves when encountering this obstacle. By default, Buildings data is treated as a solid obstacle and will be recognized in any CE prediction.

Generate a profile from NBa 02 cell object to Rx location:

- Latitude: 54.7272125

- Longitude: 25.2291091

<img src="../../../assets/images/ce-pro/training-05/image21.png" style="width:6.5in;height:3.98681in" alt="A screenshot of a computer Description automatically generated" />

The Path Loss option displays the Total Path Loss, which includes both model loss and diffraction loss.

<img src="../../../assets/images/ce-pro/training-05/image22.png" style="width:2.68788in;height:1.4377in" alt="A white background with black text Description automatically generated" />

The Buildings clutter class is specifically used to define building locations. If the path crosses this clutter class, it will be identified as a solid obstacle, and diffraction loss will be added to the final path loss value.

### Diffraction coefficient

Open Prediction Model Manager, then CEC ITU-R prediction model and 3km radius configuration. Double click on Buildings layer, and change Diffraction loss coefficient to 0.6.

<img src="../../../assets/images/ce-pro/training-05/image23.png" style="width:3.22962in;height:0.44798in" />

A lower coefficient can be applied for lower frequencies, where the signal is less affected.

- Press Apply button and draw a profile from the same cell to the same Rx location as previously. (54.7272125; 25.2291091)

<img src="../../../assets/images/ce-pro/training-05/image24.png" style="width:6.5in;height:4.00069in" alt="A screenshot of a computer Description automatically generated" />

Compare results, previously it was 34.3 dB loss, and now 20.58 dB.

<img src="../../../assets/images/ce-pro/training-05/image25.png" style="width:2.72955in;height:1.45854in" alt="A white background with black text Description automatically generated" />

Do the same for other clutter classes, as an example Forest clutter class with Diffraction loss coefficient 0.5:

<img src="../../../assets/images/ce-pro/training-05/image26.png" style="width:6.5in;height:4.02014in" alt="A screenshot of a computer Description automatically generated" />

And using Diffraction loss coefficient – 0.7, it will change Clutter loss value from 16.81 dB to 20.6 dB.

<img src="../../../assets/images/ce-pro/training-05/image27.png" style="width:6.5in;height:4.025in" alt="A screenshot of a computer Description automatically generated" />

### Penetration loss

Penetration loss describes how a signal is affected as it enters an obstacle and attenuates within it, as in an Outdoor-to-Indoor scenario. This loss includes several parameters and is only applied when the RX location falls within the specified clutter class.

- Penetration loss offset – the entry loss to clutter object.

- Penetration loss distance coefficient – how signal slope inside clutter class object.

- Penetration loss frequency coefficient – how signal slope inside clutter class based on frequency.

Draw a profile from NBb 01 cell to RX location:

- Latitude: 54.7349136

- Longitude: 25.2857285

<img src="../../../assets/images/ce-pro/training-05/image28.png" style="width:6.5in;height:3.99722in" alt="A screenshot of a computer Description automatically generated" />

Leave profile open, and open Prediction Model Manager, then CEC ITU-R prediction model and 3km radius configuration. Double click on Buildings layer, and change Penetration loss coefficient from 0 to 8 dB.

<img src="../../../assets/images/ce-pro/training-05/image29.png" style="width:3.14627in;height:0.43756in" />

Press Apply button and click Manual Profile button in Profile.

<img src="../../../assets/images/ce-pro/training-05/image30.png" style="width:4.37561in;height:0.35422in" />

Profile will be regenerated with updated Path Loss values. Penetration loss is now 8 dB higher than previously.

<img src="../../../assets/images/ce-pro/training-05/image31.png" style="width:2.68788in;height:1.48979in" alt="A white background with black text Description automatically generated" />

Change other penetration values and regenerate profile.

<img src="../../../assets/images/ce-pro/training-05/image32.png" style="width:3.16711in;height:0.84387in" alt="A screenshot of a computer Description automatically generated" />

And result is now:

<img src="../../../assets/images/ce-pro/training-05/image33.png" style="width:2.71913in;height:1.44812in" alt="A white background with black text Description automatically generated" />

Close Profile tool.

## New Prediction Model

Open Prediction Model Manager, right click on CEC ITU-R (100MHz – 6GHz) model and choose Create New.

<img src="../../../assets/images/ce-pro/training-05/image34.png" style="width:3.39in;height:1.58in" alt="A screenshot of a computer Description automatically generated" />

Define:

- Model Name: PM 1km radius

- Maximum Radius (km): 1

- Effective Earth Radius: 8500

- Receiver Height: 1.5

- Offset coefficient: 45

- Distance coefficient: 30

- Distance coefficient obstructed: 40

- Frequency coefficient: 20

- Leave clutter values as it is.

Press Apply.

<img src="../../../assets/images/ce-pro/training-05/image35.png" style="width:2.65in;height:4.68in" alt="A screenshot of a computer Description automatically generated" />

Open Object Editor for Cells NBa 01, NBa 02, NBa 03 and change prediction model to PM 1km radius for these Cells.

<img src="../../../assets/images/ce-pro/training-05/image36.png" style="width:4.81in;height:2.08in" alt="A screenshot of a computer Description automatically generated" />

Run RF predictions and preview results loaded in the Contents.

<img src="../../../assets/images/ce-pro/training-05/image37.png" style="width:3.58in;height:2.81in" alt="A screenshot of a computer Description automatically generated" />

Prediction radius will be limited to 1 kilometer.

<img src="../../../assets/images/ce-pro/training-05/image38.png" style="width:5.35in;height:4.43in" alt="A map with a colorful circle Description automatically generated with medium confidence" />

# UniMacro

UniMacro model acts similary to CEC – ITU model, just here it has additional 9999 model coefficients.

<img src="../../../assets/images/ce-pro/training-05/image39.png" style="width:3.11502in;height:1.68774in" alt="A screenshot of a computer Description automatically generated" />

Open prediction dialog, expand UniMacro model and double click on Default prediction model. Preview parameters.

<img src="../../../assets/images/ce-pro/training-05/image40.png" style="width:2.73in;height:5.15in" alt="A screenshot of a computer Description automatically generated" />

Select NBb 01, 02 and 03 cells, then right click on Cells in the contents and open Attribute Table.

Find Prediction model type ID field, right click on and choose Calculate Field.

<img src="../../../assets/images/ce-pro/training-05/image41.png" style="width:2.49in;height:1.96in" alt="A screenshot of a computer Description automatically generated" />

Define value 2 and press OK. By defining value 2, we change prediction model type for selected cells. If prediction model type is 2 – then it is UniMacro model. Here is prediction model table:

<img src="../../../assets/images/ce-pro/training-05/image42.png" style="width:4.34436in;height:1.81275in" alt="A screenshot of a computer Description automatically generated" />

Find prediction_model_configuration_id field and calculate value 1 for selected Cells.

<img src="../../../assets/images/ce-pro/training-05/image43.png" style="width:4.17in;height:0.44in" alt="A white rectangle with a black stripe Description automatically generated" />

Open Object Editor for selected Cells, double click on any cell in Object Editor and preview assigned prediction model.

<img src="../../../assets/images/ce-pro/training-05/image44.png" style="width:4.63in;height:0.37in" />

Open RF Prediction tool, and run predictions with defined parameters.

<img src="../../../assets/images/ce-pro/training-05/image45.png" style="width:3.54in;height:2.81in" alt="A screenshot of a computer Description automatically generated" />

Preview loaded results.

<img src="../../../assets/images/ce-pro/training-05/image46.png" style="width:4.9in;height:4.27in" alt="A map with a colorful explosion Description automatically generated with medium confidence" />

Open Prediction Model Manager, UniMacro model \> Default and one by one change:

- Define A0: 45, and run RF Prediction.

- Define A1: 40, and run RF Prediction.

After that, compare all three predictions using Explore tool.

<img src="../../../assets/images/ce-pro/training-05/image47.png" style="width:4.79in;height:1.15in" alt="A blue line on a white background Description automatically generated" />

# LOS ITU-R P.525 (6GHz – 100GHz)

The prediction model is dedicated to higher frequencies, usually for mmWave 5G bands. It gives the results for only LOS areas. Leave the same cells selected and open Cells Attribute Table (right click on Cells \> Attribute Table).

- Find Prediction model type ID field and using Calculate field change value from 2 to 4.

- For prediction_model_configuration_id define value 3.

- Change:

  - Power to 25;

  - Frequency to 26000;

  - Bandwidth to 200;

  - Subcarrier spacing to 60;

  - TxMIMO to 32

  - RxMIMO to 32

  - Active antenna effect to 6;

  - Frequency group: mmWave Band.

Open RF Prediction tool. Run predictions with the same parameters.

<img src="../../../assets/images/ce-pro/training-05/image48.png" style="width:4.8in;height:2.85in" alt="A screenshot of a computer Description automatically generated" />

It will provide coverage results where only LOS condition exist. Additionally, each cell will have signal strength value.

<img src="../../../assets/images/ce-pro/training-05/image49.png" style="width:6.5in;height:3.40347in" alt="A screenshot of a computer screen Description automatically generated" />
