# Atlas-Config
![image](https://user-images.githubusercontent.com/105144083/167309716-e38543bc-55df-45b6-bf4b-89d1a11c6af4.png)


This configurator does several things. When you select your ServerGrid.json file, it will pull the number of x grids and y grids, and begin to populate suggested ports that would need to be forwarded You can modify the start port and it will calculate the ending port. The ip address is retrieved from amazon aws.

Game, Query and RCON ports will do port number +1. This may be removed in future releases, but keeping in place for the moment. Seamless increments by 1 for each grid. These ports and the external ip are saved to the json. This program uses amazonaws to retrieve your external ip address.

The Populate Power Stones and Essences will set the quest entries to the correct islands. The quest location points just to the island itself, not to the specific location on the island. This option is disabled if when you specify your json it does not contai each of the PVE islands and at least 9 trenches. This will also set the quest location for the kraken if one of your grids has the extraSublevels set for EndBossLevel.

Selecting the overwrite option will overwrite all the changes to the json. This is not recommended in early versions of the program.  If you do no specify to overwrite, it will write the json next to the Beach_Atlas_Config.jar

Caveats: This program will check if you have one of each of the distinct PVE islands and 9 trenches. Currently didn't have a plan to allow for duplicating powerstone islands, but may if there is enough request for it.

**Requirements**
Requires Java Runtime Environment 8.  Available https://www.java.com/en/download/

To run, navigate to the dist folder and run Beach_Atlas_Config.jar


Beach#2483 on discord for support.

**Currently not functioning**

Using the check box for Fill in Discovery Zones will only add discovery names from the discozones text file located in the resources folder. It assigns the names from the top of the file downward, so if you decide you want some of yours assigned, put them at the top of the file. Names will be repeated if you have more discovery zones than the number of lines in the file.

The Give Server Names From Templates option will, if server templates used when creating the servergrid, make the server name be named as server template name_increment, e.g. Polar_1, Low Desert_2. This only writes to names that are not set. This option is useful if you want to give your players a heads up for what type of template the grid they are going is.

The add transient nodes check box will add cursed and sulfurous ground to the islands specified in the transient.txt file inside the resources folder. These islands were pulled from the official json, but can add additional islands to the file. This will alternate between the two transient types.


