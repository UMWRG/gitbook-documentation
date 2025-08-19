# Tour of the Interface

{% embed url="https://www.youtube.com/watch?v=gm4-EwMDwVU" %}
Video showing an overview of the Water Strategy interface
{% endembed %}

Project: Folder that contains related networks, also can contain other project folders (sub-projects).

&#x20;       \-Each project folder displays the amount of networks and sub-project folders within it.

Network: Model.



1. At the interface home page, select the “Training Material” project.
2. Select the Demo 1 network.

&#x20;       \-Inside the network, at the top of the page, you will see a bar that looks like this below.

![](<../.gitbook/assets/0 (2).png>)

&#x20;      \-The “Home” and “My Projects” tabs will bring you back to the interface homepage.

&#x20;      \-“Documentation and Training” takes you to the interfaces tutorial videos and written instructions page.

&#x20;      \-The “Favourites” tab allows you to bookmark projects, networks, and scenarios. It also                                     gives the ability to go to recently accessed and recently modified projects and networks.

&#x20;       \-“Back to ‘Training Material’” brings you back to the Training Material project folder.

![](<../.gitbook/assets/1 (2).png>)

&#x20;       \-The green play button runs a model.

&#x20;       \-The wrench button provides access to advanced network utilities, such as importing or exporting network data.

&#x20;       \-The downwards arrow into the rectangle button is for downloading the model, this is used to run offline or send to someone.

&#x20;       \-The three lines are “View Network Data”.

3. Click on “View Network Data”.

&#x20;       \-In “Details” you can change the name of the network.

&#x20;               \-Sometimes requires exiting network to update.

&#x20;       \-In “Inputs” you can change the start, end, and timestep of your model.

&#x20;               \-D=day, M=month, Y=year for timestep.

![](<../.gitbook/assets/2 (2).png>)

4. Click on the wrench icon to go to “Settings”.

&#x20;       Display labels- displays node names

&#x20;       Link direction- shows flow direction of links

&#x20;       Show Tooltips- displays node information when hovering over it

&#x20;       Auto Hide Sidebar- hides sidebar when not using it

&#x20;       Always Categorise Attributes by Type- Within a node, will group attributes as scalars, descriptors, etc.

5. Click on the “i” to go to “Info”.

&#x20;       \-You can see your “Network ID” and other information.

6. Close the sidebar and go to the scenario section on the left side of the page.

![](<../.gitbook/assets/3 (2).png>)

&#x20;       \-Scenarios are variations of input data, hydrology, etc. within a model.

&#x20;       \-Common to make multiple scenarios within a model.

&#x20;               Button 1(left)- Clone scenario

&#x20;               Button 2- Edit Scenario

&#x20;               Button 3- Delete scenario

&#x20;               Button 4- Refresh scenario list

&#x20;               Button 5- Bookmark scenario

&#x20;               Button 6(right)- Compare scenarios

&#x20;       \-To make a new scenario, clone a pre-existing scenario giving it a new name, once created change model input data as desired.

7. Click the “Run a Model” button.

&#x20;       \-Keep the baseline scenario.

&#x20;       \-Keep all other defaults.

8. Click “Submit”.

&#x20;       \-In the “Runs” section on the left side of the page you will see your new run and past runs.

![](<../.gitbook/assets/4 (2).png>)

&#x20;       \-Yellow=Run in queue

&#x20;       \-Blue=Run in progress

&#x20;       \-Green=Successful run

&#x20;       \-Red=Run failed

9. Click “Build” below the “Run” section.

&#x20;       \-This provides all the nodes and links needed to build a model.

&#x20;       \-After inserting a node, data needs to be entered.

10. Click “Search” below the “Build” section.

&#x20;       \-This allows you to easily find nodes and links in large models.

The bomb button in the upper left hand corner of the map allows you to expand your model to make it less crowded if needed.

![](<../.gitbook/assets/5 (2).png>)

&#x20;       Map- Shows model

&#x20;       Resources- Can view your nodes, links, and groups

&#x20;       Metrics- Provides functionalities for aggregation of model outputs

&#x20;       Custom Rules- Custom operating rules

&#x20;       Parameters- Add parameters not included in pywr

&#x20;       Recorders- Add recorders not included in pywr

&#x20;       Members- Shows the members who have to access to the model and the permissions they possess, can also add members in this tab and choose the permissions they have

&#x20;       Analysis- Comparing nodes and links within scenarios
