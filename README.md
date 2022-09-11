# CustomDiscordNotif
Have a sound play when you receive a new message a Discord

This program will watch a specfic point of your screen and play a sound once this point changes to a specific color.
The points, trigger colors and location of the sound (or sounds) to be played, can be configured under /config/base_config.xml in the release folder.
The settings in that config are to be set by the following:
In order to use this program, measure the pixel position of the red notification badge that discord shows on your task bar if you get a new message and use that to configure the file (a screenshot program like "greenshot" that shows the pixel coordinates works well here)

---NOTICE---
* all the configured values need to be strings. i.e. even numbers, like for **screen_index**, need to be written like "0", not 0
* the colors are configured to match the discord taskbar icon behaviours. In theory, this works with any pixel on the screen that changes, and is not bound to discord in particular
* if you need to put the program somewhere else, like on your desktop, do NOT move the actual .exe-file. instead, create a shortcut of it and move that one. the whole release-folder can be anywhere on your machine, though

* **folderpath**:
path to the folder in which your custom sounds are. The sound files HAVE to be in a .wav format in order to be played. If there are multiple sounds, it will pick a random one from the folder. 
* **screen_index**:
the index of the screen to watch for color changes at. if you only have one monitor, this will be likely "0"
* **screen_pos_x**:
the pixel position of the chosen screen to watch for changes at (from right to left)
* **screen_pos_y**:
the pixel position of the chosen screen to watch for changes at (from top to bottom)
* **color_notif_on**:
the color to check which triggers the sound - once the observed pixel has changed to this color, the sound will be played (i.e. when the notification badge appears)
* **color_notif_off**:
the color to check which resets the trigger - in order to prevent the program from spamming a sound, it will only be able to play a sound again after the pixel has turned into this color (i.e. when the notification badge goes away)
