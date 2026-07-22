# 3.1.42 Quick mesh connectivity

Click this button to open Quick mesh connectivity tool.
To enhance the efficiency of early-stage planning and dynamic mesh layout, the Quick Mesh
Connectivity tool offers a fast and intuitive way to assess connectivity potential.
This lightweight yet powerful feature enables users to instantly evaluate whether a Mesh Node can
connect to an existing mesh network based on either its current position or a proposed location.
Whether you are planning the deployment of a single node or simulating a mobile mesh scenario, Quick
Mesh Connectivity streamlines the decision-making process by providing immediate, actionable feedback.

![Image p232](../../../assets/images/ce-express/user-guide-v73/p232-img1.png)

![Image p232](../../../assets/images/ce-express/user-guide-v73/p232-img2.png)

Calculation settings
Mesh node template
The Mesh Node Object Template is automatically utilized whenever a Mesh object lacks the required
parameters needed to complete connectivity calculations. This ensures that all essential data is available

![Image p233](../../../assets/images/ce-express/user-guide-v73/p233-img1.png)
for accurate simulation and evaluation, even if the original Mesh object is incomplete.
Temporary mesh node template
The Temporary Mesh Node Object Template is automatically utilized whenever a newly proposed Mesh
object lacks the required parameters needed to complete connectivity calculations. This ensures that all
essential data is available for accurate simulation and evaluation, even if the original Mesh object is
incomplete.
Temporary mesh node
X
Coordinate in the projected coordinate system.

Y
Coordinate in the projected coordinate system.
Height
Mesh node object’s height above the terrain.
Antenna
Antenna which will be used for Mesh node.
Prediction model
Prediction model used to calculate a path loss between Mesh Nodes.
Frequency
Frequency in MHz for proposed Mesh Node.
Power
Tx power in dBm for proposed Mesh Node.
Misc. Loss
Total losses in dB for proposed Mesh Node.
Sensitivity
Receiving Signal Level threshold in dBm at Mesh Node.
3.1.42.1 Calculate Quick mesh connectivity
- Select Existing Mesh Nodes
On the map interface, select the Mesh Nodes that should be included in the connectivity calculation.

- Open the Quick Mesh Connectivity Tool
- Configure Node Parameters
Input the required parameters for the proposed Mesh Node (e.g., transmission power, antenna type,

![Image p235](../../../assets/images/ce-express/user-guide-v73/p235-img1.png)

![Image p235](../../../assets/images/ce-express/user-guide-v73/p235-img2.png)
height).

- Define the Proposed Node Location
Choose the location of the new Mesh Node either by clicking directly on the map or by entering specific

![Image p236](../../../assets/images/ce-express/user-guide-v73/p236-img1.png)

![Image p236](../../../assets/images/ce-express/user-guide-v73/p236-img2.png)

![Image p236](../../../assets/images/ce-express/user-guide-v73/p236-img3.png)
coordinates.
- View the Results
Once the analysis is complete, the results will appear on the map:
- Green indicates areas with successful two-way connectivity.
- Yellow shows one-way connectivity.
- Red marks areas with no connectivity.
