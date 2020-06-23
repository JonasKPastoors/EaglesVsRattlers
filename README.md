# Eagles Vs Rattlers Research Prototype

## Description
The Eagles vs Rattlers Prototype is a piece of software that has been used to collect data for the the thesis “*The Opposite of Love: How parasocial interaction with NPCs can be enhanced through intergroup competition*” (Pastoors, 2020) and is made available for further research, as well as replication. It utilizes similar methodology as previous studies by Cikara et al. (2014) and Hudson et al. (2019) to study intergroup empathy bias in video game players.

While the software is a prototype, it is functional and can be used for further study and replication. However, ideally it should be refactored before further use in order to improve performance, usability, as well to fix known issues.

A running version of Eagles vs Rattlers can be accessed via [itch.io](https://halbglutprinz.itch.io/eaglesvrattlers?secret=aSpBJkqiPIXMeRjCTVprXdol8).

## Important notice
When downloading this repository, the .zip files should be downloaded individually to avoid data corruption.
![](https://i.imgur.com/Z5Yql2w.jpg)
![](https://i.imgur.com/Xi6LYfI.jpg)

## Prerequisites
* The prototype has been created with Unreal Engine 4.23. It can run with newer versions, but has not been tested.
* To run this project Visual Studio 17 or newer, using the setting recommended in [this](https://docs.unrealengine.com/en-US/Programming/Development/VisualStudioSetup/index.html) guide is required.

## Installation
* Download [Unreal Engine](https://docs.unrealengine.com/en-US/GettingStarted/Installation/index.html) (Make sure you have version 4.23)
* Download the prototype .zip file
* Unpack zip on your computer
* Open folder and double click *UE4_EaglesVRattlers.uproject*

## Data Collection
The data collection in Eagles vs Rattlers is conducted via an API and sends its results to the portal [GURaaS.com](https://guraas.com) (Santos et al., 2017). In order to gather data via the same means, please get in contact with [Dr. Carlos Pereira Santos](https://pure.buas.nl/en/persons/carlos-pereira-santos), in order to get access to the tool.

Within the prototype data is sent via the plugin Data Logger (Galdieri, 2019), which is turned off by default. To activate Data Logger, open the project and go to 
> Edit (in the top bar) -> Project Settings -> scroll down to Plugins -> Data Logger

Check the box “Is Enabled” and make sure you enter the correct GURaaS ID into “Game ID”.

![How to](https://i.imgur.com/tVZXX9K.png)

GURaaS will not yield data that is directly compatible with SPSS (or other analysis tools). The attached Microsoft Excel spreadsheet (EvR_GURaaS-SPSS_Converter) can help circumvent this issue (if the logged parameters are the same as in Eagles vs Rattlers Version 1.1) and bring the data automatically into the correct format.

To use the spreadsheet, the .json file yielded by GURaaS first needs to be converted into an .xlsx (or similar) file. Afterwards, copy the raw data into the “*Raw Data*” spreadsheet (make sure “*session ID*”, “*time*”, etc. are in  the correct column) and hit the button. The correctly formatted results can be accessed in the “*results*” spreadsheet in the same file.

## Creating and hosting a build
In order to create a custom build go to:
> File (in the top bar) -> Package Project -> HTML 5

To host the project on itch.io, delete “*readme.txt*”, “*RunMacHTML5LaunchHelper.command*”, and "*HTML5LaunchHelper.exe*". Make sure to rename the .html file to index.html (the capitalization is important). How hosting the build on other platforms works has not been tested.

A .pdf file with all settings used for hosting on itch.io has been attached. To test hosting on itch.io without having to create a build, a host-ready build is included in the repository (the logging of data is turned off in that one).


## Known Issues
There are a few known issues Eagles vs Rattlers has. For an in-depth explanation of the following needed improvements please consult chapter 3.3.3 Software in the corresponding Master’s Thesis (Pastoors, 2020).

* Bug: Occasionally, participants will not be able to answer the questions on the last slide with catch-questions in the build-version. * The cause of this is currently unknown.
* Bug: Occasionally the AI will not move and end their turn prematurely. The reason for this is currently unknown.
* Bug/Improvement: The teams have too many NPCs each in a playthrough. The number of NPCs in a playthrough should be restricted to four each.
* Improvement: The mix of NPC-faces in each team is not reliably unbalanced. In the future a mechanism should be included that distributes racial and gender representations evenly among the teams.
* Improvement: If the prototype is used on workers from the platform MTurk, participants should be asked for their worker ID at the beginning of the experiment, in order to ensure the fair payment of everyone involved.

## Citation
Pastoors, J. K. (2020). Eagles vs Rattlers (Version. 1.1) [Research Prototype]. Breda, NL: Breda University of Applied Sciences.

## Contact
If any issues should arise, please contact me via my website [www.jonas-pastoors.com/contact](https://www.jonas-pastoors.com/contact)

## References
Cikara, M., Bruneau, E., Van Bavel, J. J., & Saxe, R. (2014). Their pain gives us pleasure: How intergroup dynamics shape empathic failures and counter-empathic responses. Journal of Experimental Social Psychology, 55, 110–125. doi: 10.1016/j.jesp.2014.06.007.

Galdieri, R. (2019). Data Logger (Version. 1.1) [Unreal 4 Plugin]. R. Galdieri.

Hudson, S.-K. T. J., Cikara, M., & Sidanius, J. (2019). Preference for hierarchy is associated with reduced empathy and increased counter-empathy towards others, especially out-group targets. doi: 10.31234/osf.io/4kc3y.

Pastoors, J. K. (2020). The Opposite of Love: How parasocial interaction with NPCs can be enhanced through intergroup competition. researchgate.net. Retrieved June 16th, 2020, from https://www.researchgate.net/publication/342134174_The_Opposite_of_Love_How_parasocial_interaction_with_NPCs_can_be_enhanced_through_intergroup_competition. doi: 10.13140/RG.2.2.31175.52642.

Santos C. P., van de Haterd J., Hutchinson K., Khan V.-J., Markopoulos P. (2017) GURaaS: An End-User Platform for Embedding Research Instruments into Games. In: Barbosa S., Markopoulos P., Paternò F., Stumpf S., Valtolina S. (eds) End-User Development. IS-EUD 2017. Lecture Notes in Computer Science, vol 10303. Springer, Cham.

## Acknowledgements
I would like to thank Giandomenico "gmilh" Lombardi for helping me debug, as well as upload the prototype and build.
