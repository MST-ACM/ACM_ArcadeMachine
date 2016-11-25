# ACM Arcade Machine Documentation
This repository includes the documentation on general structure of the ACM Arcade Machine's programs, procedures in order to resolve any future issues, and additional resource backup for the Arcade Machines Files

## Dependencies
1. [Mame](http://www.mame.net/)
  + ```Mame``` - The emulator program which is used to actually run the games. All games can be found under the ```MAME/roms``` file.
2. [mGalaxy](http://www.mgalaxy.com/)
  + ```mGalaxy``` - The menu program which reads the gamees under the ```MAME/roms``` and displays them in the main list.
  + ```Configuration``` - All configuration of mGalaxy is done by running ```mGalaxy_runaway``` program located on the ```mGalaxy``` folder.
3. [WiniPAC](http://www.ultimarc.com/winipac_ipd.html)
  + ```WiniPAC``` - The program which handles the inputs from the button/joysticks, converts them into normal keyboard characters, and sends them as a keepboard input to the computer
  + ```Configuration``` - The configuration is done by starting the WiniPAC program, changing keybinds using the GUI, and hitting the program button located at the bottom right of the GUI
    + ```NOTICE:``` The ```acm.ipc``` configuration file located in ```C:\Program Files\WinIPAC``` is advised as it already works within the confines of ```Mame```, ```mGalaxy```, and ```WiniPAC```. Backup located in this repository [acm.ipc](acm.ipc).
    + In order to restore, simply download the [acm.ipc](acm.ipc) file, run the file, and then hit program at the bottom right of the ```WiniPAC``` GUI.

***

## Startup Flow
1. In Windows XP, the startup folder runs the mGalaxy startup and the [program_ipac](program_ipac.bat) file.
2. [program_ipac](program_ipac.bat) starts WiniPAC in ```C:\Program Files\WinIPAC``` with [acm.ipc](acm.ipc) configuration file located within that directory.
  + This begins WiniPAC with the acm.ipc configuration that allows the joysticks/buttons to send the proper signals to ```Mame```.
3. ```mGalaxy``` starts and loads all of the games located within the ```MAME/roms``` folder alphabetically in the list.
4. A user selects a game from the ```mGalaxy``` list and ```Mame``` emulates the game until it is closed.
5. After the game is closed, ```mGalaxy``` reopens at the point in the list the user ended on.

***

## Troubleshooting
### Buttons/Joysticks not committing expected actions
1. Run the ```mGalaxy_runway``` program and click on the ```Defaults``` option located on the GUI
2. Download the [acm.ipc](acm.ipc) backup configuration file and overwrite the configuration in ```C:\Program Files\WinIPAC```
3. Open the [acm.ipc](acm.ipc) file on the computer and hit ```Program``` on the ```WiniPAC``` GUI.
4. Restart the computer.

### 'Cannot Program' Dialog opens in WiniPAC GUI
1. Open the ```WiniPAC``` GUI if not already open.
2. In the bottom right of the GUI, click on the ```options``` button
3. Go to the section which lists the different type of ```IPAC devices``` and cycle through the three selections until one works. (I cannot remember off the top of my head, if you encounter this issue please updates).

### Other issues
1. The [First Troubleshooting](#Buttons/Joysticks not committing expected actions) option should work for most issues.
2. If it does not work please contact [acm@mst.edu](acm@mst.edu) to fix it.
3. If you fix a problem not listed or without any of these steps, please document it here.

***

# Contributing
Please contact [acm@mst.edu](acm@mst.edu) if you wish to improve, help, or mantain the Arcade Machine and its documentation.
