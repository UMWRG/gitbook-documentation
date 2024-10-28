# Adding Nodes and Links (Edges)

Nodes and links (also called ‘Edges’) are fundamental components of the water system model. Nodes represent specific elements within the system, such as reservoirs, catchments, and demands, each with unique properties, which are referred to as attributes. For example, one attribute is the ‘max\_flow’ which is the maximum flow through a node.

These attributes can be of different types (e.g. monthly profiles) and they dictate the behavior of the specific node.

Edges represent the connections or pathways through which water flows between nodes, representing rivers, pipelines, or channels. Together, nodes and edges form the structure of the network, defining how water moves through the system.

The video below can help you follow the steps below.

{% embed url="https://youtu.be/ub-fv-0u10A?t=122" %}

1. Click on the network you created in the first step, ‘My new network’

![](<../../../.gitbook/assets/0 (10).png>)

This opens the network. If you selected to display a map when creating the network, a map will be shown.

![](<../../../.gitbook/assets/1 (10).png>)

1. Zoom to a location on the map where you want to build a network. We will zoom to the Nile river in Sudan. Next click on the **Build** icon outlined in Red to view the nodes palette showing the available list of Nodes.
2. Drag and drop the nodes to be used. In this case we will use:

* 1 **Catchment** - which will represent water flowing into the system

![](<../../../.gitbook/assets/2 (9).png>)

* 1 **Link** - a connecting node

![](<../../../.gitbook/assets/3 (9).png>)

* 2 **Output** nodes - These nodes remove water from the system. One will be a demand node and the other will be a river outlet or "sink".

![](<../../../.gitbook/assets/4 (9).png>)

<figure><img src="../../../.gitbook/assets/image (22) (1).png" alt=""><figcaption></figcaption></figure>

1. To connect the nodes, click on **edge** to enable link mode. Click on the start node (catchment) and then click on the end node (link). Nodes must be started from the upstream node and ended on the downstream node.

**Please note:** once you have created the connections, click again on **edge** again to disable link mode.

<figure><img src="../../../.gitbook/assets/image (21) (1).png" alt=""><figcaption></figcaption></figure>
