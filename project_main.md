# project_main.lua dissection

## Lines 1 to 23

In these lines the code is just copyrights comments and requirements (i.e. other source code files and libraries).

## Lines 24 to 119

### Init function

1. Lines 26 to 35

Skrovet initialization, setting up skrovet system, window name and size, fonts...

2. Lines 36 to 39

This only matters if you're not running the game on the release version, thus only if you are the game dev or got a build from him.

3. Lines 40 to 54

These lines check if the settings are loaded in already or not. If not, it loads the setting, else it checks for the settings file, try to go across it to retrieve settings, if it can't, then it results in an error and the game cannor start.
After this, it saves the init settings.

4. Lines 56 to 83

Sets up the game window, puts it in fullscreen if needed.
Loads the audio files and background textures.

5. Lines 85 to 99

Keybinds setup

6. Line 100

Start to account for inputs

7. Lines 102 to 108

Sets up flagNames : solid, jump through, ladder, death, handle, drops, spores.

8. Line 110

Sets font height.

9. Lines 112 to 118

Defines sm as the state machine and use it to put the program in the intro state.

## Lines 120 to 136

10. Lines 120 to 136
