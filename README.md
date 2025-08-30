# AscentDX-dissection
In this repo, I will be documenting the dissection of the game Ascent DX in order to try to mod it


## Time management

### 1. progress_time
progress_time is a boolean, it shows up in 3 places in the entire source code.
- game_state.lua ; line 19 ; gets set to true
- outro_state.lua ; line 23 ; gets set to false
- platformer.lua ; line 681 ; increments progress.time by _dt

To change the game speed, we would then need to mess with the platformer.lua file or with the _dt value.

## Actually slowing down the game

In the platformer.lua file, the progress time gets incremented, we can add a factor the the _dt value to slow down the progress time growth. In the same file, the function make_player contains the player's behaviors with different inputs. The dash sets the x velocity to 2 times the direction (so 2 or -2 for the duration of the dash, i.e. 10 frames, given that the walking speed is .5 or -.5). We can therefore apply a factor to the x velocity and divide the frame ammount by the same factor, so to slow the game down, we would need to apply a .5 factor to the x velocity and a 2 factor to the frame ammount.
