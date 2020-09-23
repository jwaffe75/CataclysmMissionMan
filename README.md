# CataclysmMissionMan

- MissionMan for Homeworld 1 and Cataclysm does work on Windows 7 x64.
- You can install it from the game CD.

# Quirks inherited from the Homeworld 1 version of MissionMan

## 1. Level name and mission name must match, and level name must match the name of the folder the map is stored in
- E.g., that if your folder is named Test8, the level must also be named Test8, not "Test"
- If all three of these names don't match your map will not show up in the Multiplayer menu
- Note that the Level "Info" is what shows in the map selector in the multiplayer menu.
- The default text for "Info" is not very helpful or distinctive, you should change it so you can find your map when you test it.

## 2. Remember to click on the top level node (the mission node) before doing File -> Generate to generate everything

## 3. Remember that maps that support different numbers of players have one map per configuration
- As in, if your map supports 2, 3, or 4 players, you'll have a Test2 folder, a Test3 folder, and a Test4 folder

## 4. If you open Tools -> Options, the editor will crash instantly unless you close it with the X button or Cancel
- I am not sure why this is.
> Run-time error '5': Invalid procedure call or argument


# Behavior to the Cataclysm version of MissionMan
Unfortunately it seems like there's quite a few oversights in the version of MissionMan distributed with Homeworld Cataclysm

Note that the Cataclysm Mission.doc document in the same directory as MissionMan.exe is not a copy/paste of the HW1 one, and it's quite a bit more helpful.

## 1. Upon creating a new mission, the MissionSpheres are set to the wrong civs.

- For every MissionSphere, change the name to RACE_SECT, sMothership, and make sure you change the mothership ship to RACE_SECT,sMothership under the missionsphere.

## 2. MissionMan does not generate the .dist files for the resources, but they are absolutely required

- I recommend copy/pasting the dist files from the demo map into your own maps.

- If these dist files aren't present, the game will crash when the map loads.

## 3. MissionMan does not set a dist on the resources

- So that means, for every Asteroid / etc node you add to the ResourceSphere, you should manually type in the dist file that you want to use in MissionMan in that resource's distribution.

- If even one resource doesn't have a distribution set, the game will crash when the map loads

## 4. It seems like occasionally MissionMan deletes the "ExcludeShips: RACE_KUSHAN,All" node
- This is really not good because the game will crash without it being present.

## 5. Boxes show up instead of ship models
- HW1's MissionMan was able to show the ships in wireframe, but the Cataclysm editor does not seem to be able to do this.
- It looks like Barking Dog's screenshot from Mission.doc does show ship wireframes, so maybe there's a way to configure it to work

# Random Trivia
- You can actually give ships as units to the MissionSpheres even if the race's ExcludeShips is set.

## Stupid stuff (not recommended)
- You can give a Kushan or Taidan carrier to a Somtaaw / Beast Missionsphere, and recons can dock with it to repair (but not workers)
- However hitting Build will crash the game instantly unless your command ship is selected
- Having a carrier that the civ is not supposed to have screws up the Systems menu
