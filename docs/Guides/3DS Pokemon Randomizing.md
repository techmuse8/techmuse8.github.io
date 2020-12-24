
3DS Pokemon Randomizing 
=======================

Introduction
------------

This guide will show you how to randomize 3DS Pokemon games that works
on macOS, Windows and Linux using LayeredFS so you won't have to rebuild
the game entirely as a CIA.

What you need:

On your PC/Mac:

-   The latest version of
    [UPRZX](https://github.com/Ajarmar/universal-pokemon-randomizer-zx/releases)

-   The latest version of [Java](https://www.java.com/en/download/)

On your 3DS:

-   Custom Firmware (see [3ds.hacks.guide](https://3ds.hacks.guide) if
    you don't already)

-   The latest version of
    [GodMode9](https://github.com/d0k3/GodMode9/releases/tag/v1.9.2pre1)

Section I - Dumping the game
----------------------------

If you have a physical copy:

​1. Power on your 3DS while holding Start to boot into GodMode9

​2. Insert the gamecard of the game you want to randomize

​3. Navigate to [C:] GAMECART

![title](../Images/gamecarddump.png)

​4. Select `[titleid]_v##.3ds`, then select "Copy to 0:/gm9/out"

![title](../Images/gamecardgm9cpy.png)

-   This process will take some time to finish

Your dump will be in /gm9/out on your SD Card as `[titleid]_v##.3ds`

If you have a digital copy:

​1. Power on your 3DS while holding Start to boot into GodMode9

​2. Highlight [A:] SYSNAND SD, then Press R+A to open the drive options,
then select "Search for titles" ![title](../Images/digitaldump.png)

​3. Press A to go to the title list

​4. Select your game from the title list, select "TMD file options...",
then select "Dump CXI/NDS file" ![title](../Images/titlelistbase.png)
![title](../Images/digitalcxi.png)

-   This process will take some time to finish

Your dump will be in /gm9/out on your SD Card as
`[titleid] TitleName (ProductCode) (Region).cxi`

Section II - Dumping the update
-------------------------------

​1. Repeat steps 2-3 of the digital dumping guide from Section I

​2. Select the update title for your game starting with the title ID
"0004000E"

3. Select "TMD file options...", then select "Build CIA (standard)"
![title](../Images/updtmd.png) ![title](../Images/updcia.png)

-   This will also take some time to finish

Your update dump will be in /gm9/out on your SD Card as
`[titleid] TitleName (ProductCode) (Region).cia`

Section III - Randomizing the game
----------------------------------

1.  Power off your 3DS and insert your SD Card into your Mac/PC

​2. Copy the .3ds (.cxi if you did a digital dump) of your dump and the
.cia update dump to a folder on your computer
![title](../Images/copydump.PNG)

​3. Launch `launcher.jar`, select "Open ROM", then navigate to where
you placed your game dump

​4. Select Settings, then select "Load Game Update", then select where
you placed your update dump

​5. Select your options and when you are finished, click "Randomize
(Save)", then save the folder to somewhere on your computer

​6. Copy the Title ID folder of the randomized game to /luma/titles on
your SD Card ![title](../Images/layeredfs.PNG)

Section IV - Applying the randomizer patch
------------------------------------------

​1. Take the SD Card out of your computer and put it into your 3DS

​2. Power on your 3DS while holding Select to boot into the Luma
configuration menu and enable `Enable Game Patching` if its not already.

Now when you launch your game, it should be randomized if you did
everything correctly!

Credits to Ajarmar for this fork from the regular UPGR. If you deserved
to be mentioned here open a PR. ![title](../Images/randomizes.gif)

* * * * *

Documentation built with [MkDocs](https://www.mkdocs.org/).
