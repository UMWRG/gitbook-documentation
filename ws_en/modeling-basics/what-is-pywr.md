# What is Pywr?

Pywr is a free and open-source Python language software library that allows building high quality (detailed and accurate) simulation models of water resource systems.

Pywr models run quickly on your computer or, in the case of WaterStrategy, on the cloud. They can represent small water resource systems, like a city’s water supply, or very large ones, like river basins that span several countries with hundreds of water users and infrastructure assets. Pywr can simulate short periods (like a few months) or longer ones (like 100 years) at a range of time steps (from daily to monthly).

Here's a summary of the Pywr modeling process:

1\. Set up the model

First a spatial water system map and associated hydrological and water demand data are needed. WaterStrategy helps you create this network map of all the locations ('nodes') where water is entering the system (‘inflows’), where water is being used (‘water demands’), and where water is managed (locations of infrastructure). These nodes form a network connected by rivers, canals or pipelines (Pywr calls these ‘links’ or ‘edges’). Once you’ve set up your network map, you provide water supply and demand data (typically as time-series).

2\.  Run a simulation

When all the data is entered, including time-step and time-horizon, the model is ready to simulate (i.e., step through time and perform water accounting throughout the system). At the beginning of each time-step the computer begins by injecting water into all the inflow locations, then this water is routed down the network and allocated to the different water demand and infrastructure locations. This allocation process is performed with a computing technique called linear programing. After one time-step is finished, the model updates storages, records which locations got how much water, then continues to the next time-step until the end of the simulated time-horizon.

Each water demand node is assigned a priority to represent water allocation in the model. Each node has an associated penalty, and the allocation algorithm distributes water throughout the network to minimise the overall penalty. This simple approach allows for fast and maintainable simulations which have the flexibility to represent detailed and realistic water management rules.

3\. Review results

Model outputs include how much water enters each location (node) and how much is stored, consumed or passes through it in each time-step. This allows tracking how infrastructure is being used, and whether cities, ecosystems, irrigation areas, power plants, etc. are getting enough water. Results create a detailed picture of how the water management system is working and how water benefits are distributed.

Initially models are poorly parameterised and produce inaccurate predictions (the 'garbage in, garbage out' phase). Over time however, as the model is improved ('calibrated'), it can become a valuable digital twin to help operate or plan a water system. The tool helps your organisation rapidly and inexpensively evaluate the impacts of potential future water changes and interventions, and make good decisions.&#x20;

Good luck!
