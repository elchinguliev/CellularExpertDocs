# 3.1.41 Mesh connectivity

Click this button to open Mesh connectivity tool.
This tool enables rapid and accurate assessment of wireless peer-to-peer link quality during mesh network

![Image p227](../../../assets/images/ce-express/user-guide-v73/p227-img1.png)

![Image p227](../../../assets/images/ce-express/user-guide-v73/p227-img2.png)
planning and optimization.
Calculation name
Name of the calculation that will be displayed in the Prediction history.
Mesh node template
Mesh node template if selected features won’t have all necessary parameters.
How It Works:
- Select one or more Mesh Nodes in the workspace.

- Open Mesh Connectivity tool.
- Define:
o Calculation name
o Mesh node template
- Press Calculate button to start simulation.
- The tool calculates the RSL between each node pair and compares it against the configured RSL
sensitivity threshold defined for the Mesh Node object.
- Open Prediction history tool.

![Image p228](../../../assets/images/ce-express/user-guide-v73/p228-img1.png)

![Image p228](../../../assets/images/ce-express/user-guide-v73/p228-img2.png)

Connectivity status is then visually rendered using a clear, color-coded scheme:
o Green : Bi-directional connectivity – both nodes meet or exceed the RSL sensitivity for each
other.
o Yellow: Uni-directional connectivity – only one node meets the RSL threshold for the other.
o Red: No connectivity – RSL falls below the sensitivity threshold in both directions

![Image p229](../../../assets/images/ce-express/user-guide-v73/p229-img1.png)

![Image p229](../../../assets/images/ce-express/user-guide-v73/p229-img2.png)

![Image p229](../../../assets/images/ce-express/user-guide-v73/p229-img3.png)

![Image p229](../../../assets/images/ce-express/user-guide-v73/p229-img4.png)

Results:
- All results – It shows all possible combinations of Mesh network connections.
- Connections – opens new dock on the right where you can create links.
- Connection lines – Shows Mesh connections where the tool will create Link objec
To create a Links between Mesh Nodes, define Mesh connectivity results. Once result is selected, it will

![Image p230](../../../assets/images/ce-express/user-guide-v73/p230-img1.png)
add possible options to create a links between Mesh Nodes

![Image p231](../../../assets/images/ce-express/user-guide-v73/p231-img1.png)

![Image p231](../../../assets/images/ce-express/user-guide-v73/p231-img2.png)
Links creation
Delete existing links
If selected, existing links that have been created from mesh connectivity results will be deleted.
Create only enabled links
If checked, the links will be created only from the checked connectivity lines in the suggested list.
Enable/Disable Links from the suggested list

Once parameters are set, press Create links button to create Links between Mesh objects.
