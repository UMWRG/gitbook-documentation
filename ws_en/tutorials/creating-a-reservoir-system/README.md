# Creating a Reservoir System

In this tutorial you will learn how to add new infrastructure to a model including a reservoir, treatment plant and a groundwater source that will supply a demand.

Please note that there are two nodes in WaterStrategy and Pywr that represent reservoirs. The first is a **storage** node and the second is a **reservoir** node.

Both nodes store water. The reservoir node works just like a storage node, however it has built in parameters allowing you to define _evaporation_ and _precipitation_ directly on the node. To represent _evaporation_ and _precipitation_ with a storage node, a catchment and output node are required.
