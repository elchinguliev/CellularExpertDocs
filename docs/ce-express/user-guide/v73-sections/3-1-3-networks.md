# 3.1.3 Networks

Click this button to open Networks tool.
The networks tool allows for easy management of multiple objects, grouped into networks. Networks can
be defined by feature attribute or via the selection of the features required. Then, feature attribute change

![Image p53](../../../assets/images/ce-express/user-guide-v73/p053-img1.png)

![Image p53](../../../assets/images/ce-express/user-guide-v73/p053-img2.png)

![Image p53](../../../assets/images/ce-express/user-guide-v73/p053-img3.png)
tracking and calculations can be performed for each network without the need for selection.
Once expanded, an existing network item displays the following information:

![Image p54](../../../assets/images/ce-express/user-guide-v73/p054-img1.png)
Feature type
The feature type associated with the network.
Feature count
Total feature count in the network.
Uncalculated features
Number of [Network objects](#kw:object-types:ce-express-network-objects) that have not yet been added to a calculation.
Calculation status
Status of the current calculation.
Last calculated
The last time the calculation was started.
Results
Select which [prediction results](#kw:viewing-results:ce-express-rf-prediction) you want to add to the Map view and manage in the layers tool.

Export
Exports the selected [prediction results](#kw:viewing-results:ce-express-rf-prediction) layer as a TIF raster.
Open
Opens the selected [prediction results](#kw:viewing-results:ce-express-rf-prediction) layer.
Upon hovering the mouse over a network item, options for it appear.
Edit Network
Network publishing settings
Delete Network
3.1.3.1 Add network
To create a network press the New network button.

Network name
The name of the network
Feature type
The type of feature to be included in the network.
Feature filter
- By attribute – Include features in the network by selecting an attribute and inputting the required
attribute values. The features with these values will then be filtered and included in the network.
- From selection – Include features in the network from the currently selected items.
Attribute
The attribute field to be filtered by.
Filter attribute values
Required values for the filter attribute. Features containing ANY of the entered values will be included.
3.1.3.2 Network publishing setting
If you would like the calculation results to be automatically published when the network is re-calculated,

![Image p56](../../../assets/images/ce-express/user-guide-v73/p056-img1.png)
you may set it up in the network publishing settings menu.
First open the calculation result layer you would like to be automatically published, and set up the color
band values as per your preference:

Then, options for your layer‘s publishing will appear under the calculation results section:

![Image p57](../../../assets/images/ce-express/user-guide-v73/p057-img1.png)

You may enable automatic publishing and select who the results are shared to for this layer.
The same options are also available for the features that are associated with the network.
After setting up the automatic publishing options, click Accept to save. The publishing is then executed

![Image p58](../../../assets/images/ce-express/user-guide-v73/p058-img1.png)

![Image p58](../../../assets/images/ce-express/user-guide-v73/p058-img2.png)
the next time the network calculation is run.
