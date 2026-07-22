# 3.1.40 Mesh topology builder

The mesh topology builder tool optimizes the process of making a connection between 2 desired mesh
nodes.
The tool first analyzes the possible link between the 2 selected nodes, and if a direct connection is
possible, it prompts you to create the link object between them.:

![Image p225](../../../assets/images/ce-express/user-guide-v73/p225-img1.png)

![Image p225](../../../assets/images/ce-express/user-guide-v73/p225-img2.png)

If a direct connection is not possible, the tool will automatically run an optimal placement prediction
between the 2 nodes and show you the resulting raster. You are then prompted to select a location for an
intermediate mesh node with the help of the displayed optimal placement layer, and quick mesh
connectivity lines for the location you choose. (SS)
Once a new intermediate node location is chosen, you can click Place intermediate mesh node to create
it, at which point a new process is started between the new node and the unconnected link from it. If all
connections are possible, the tool prompts you to create links for the multi-node path, at which point the

![Image p226](../../../assets/images/ce-express/user-guide-v73/p226-img1.png)

![Image p226](../../../assets/images/ce-express/user-guide-v73/p226-img2.png)
originally selected mesh nodes are connected through a series of intermediate mesh nodes.
