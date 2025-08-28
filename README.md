# AscentDX-dissection
In this repo, I will be documenting the dissection of the game Ascent DX in order to try to mod it


## Time management

### 1. progress_time
progress_time is a boolean, it shows up in 3 places in the entire source code.
- game_state.lua ; line 19 ; gets set to true
- outro_state.lua ; line 23 ; gets set to false
- platformer.lua ; line 681 ; increments progress.time by _dt
