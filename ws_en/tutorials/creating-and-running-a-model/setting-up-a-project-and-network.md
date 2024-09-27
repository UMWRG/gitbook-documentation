# Setting up a Project and Network

This tutorial introduces first steps in WaterStrategy, including:

* **creating a project and a network**,
* adding different types of nodes including a catchment node and water demand represented by an output node,
* **adding data** to the nodes
* creating two different **scenarios**, and
* **visualizing and comparing** modelled time-series outputs between the scenarios

Please follow the steps below. The video also details the steps in this tutorial. Please note that the placement of nodes in the video is different to the screenshots below. Please follow the screenshots and use the video as a guide on how to implement the steps.

{% embed url="https://youtu.be/I0SZ9GXLmXk" %}

### Create a Project

Creating a project in WaterStrategy is essential for organizing and managing water system modeling effectively. Projects provide a structured environment for organizing related models, scenarios, and data, making collaboration easier. They store input data, model configurations, and simulation results in one place. Projects also promote reusability by allowing components and input file data to be reused across multiple models, saving time and effort.

1. In the [‘My projects’](https://hydra.org.uk/projects) page, click on **Create Project.**

![](<../../.gitbook/assets/0 (8).png>)

We will name this Project “My First Project”. You can add a description if you would like. Then Click **Add.**

![](<../../.gitbook/assets/1 (8).png>)

"My First Project" has been created. Within this project, users can create different network versions and upload files such as input data, which will be shared among the networks within the project.

### Create a Network

Creating a network in WaterStrategy is essential for structuring and defining the components of the water system model. Networks represent the physical and conceptual layout of the system, with each network embodying a specific topology or connection of nodes, such as reservoirs, catchments, and demand nodes. By creating a network, users visually map out the connections between these components. This is called the model **topology**. This helps users understand how water flows through the system and how different elements interact.

Networks in WaterStrategy promote collaboration and efficiency. Once a network is created, it can be shared with team members, enabling users to work on the same network or give their colleagues their on copy of a network.

Additionally, creating a new network from an existing one is easy – users can simply clone an existing network and then apply modifications to it. This flexibility allows users to quickly iterate on their models, test various hypotheses, and evaluate different management strategies.

1. Click on “My First Project” to go into it

![](<../../.gitbook/assets/2 (7).png>)

1. Click on **Create Network**.

![](<../../.gitbook/assets/3 (7).png>)

1. Click on **Manual**

![](<../../.gitbook/assets/4 (7).png>)

add a Name and optionally a Description to your Network.

Choose your Template, in this case _Pywr child template v1 (March 2021) – flow units in Mm3/day_.&#x20;

“Use Map” should be selected to show map background layer in the network.

1. Click **Submit**.

“My New Network” is now created!.

![](<../../.gitbook/assets/5 (6).png>)
