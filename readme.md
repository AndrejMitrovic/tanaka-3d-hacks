# Tanaka 3D

This repo contains some information about how to run Tanaka 3D,
and also how to modify the game files to get extra credits,
vehicles, etc.

# Installing

To play this game on Windows 10:
- Download the Tanaka Demo on archive.org (https://archive.org/details/TANAKA_201402)
- Download the Tanaka MAC ROM on oldgamesdownload.com (https://oldgamesdownload.com/file/88546-2/)
- Install the Demo.
- From the zip file Tanaka_Mac_ROM_EN.zip extract the files 'resources.omt', 'prefs.omt', and 'pilots.omt. Extract them into 'C:\Program Files (x86)\Pacific Media WorX\Tanaka 3D Demo' and overwrite the existing files.
- Right click Tanaka.exe in 'C:\Program Files (x86)\Pacific Media WorX\Tanaka 3D Demo', select Compatibility tab, and select 'Run this programin in compatibility mode for: Windows 95'
- The game will now run. Although it's still buggy as using the keyboard/mouse in the main menu can sometimes crash. But the game is still playable.
- It's possible to set it to a higher resolution through its settings.

# Hacking game files

The `C:\Program Files (x86)\Pacific Media WorX\Tanaka 3D Demo\pilots.omt` contains the save file.

It seems to contain the active level the player reached, and the credits, vehicles, etc.

## Credits

The `0x00000019` and `0x0000001A` bytes:

These used to store the credits amount as a 2-byte number.

Probably 0xFFFF would give you the maximum credits of 65535.

## Engine

The `0x00000044` and `0x00000045` bytes.

These are used to select the engine.
Lower numbers are slower engines.

Max engine is 0x0900 (set from game)

## Car

The `0x00000044` byte stores the car.

There's only a small number of possible cars, so it's only stored in one byte.

The fastest car option is 0x09.

## Level (work in progress, not validated)

The 0x0000005B and 0x0000005C bytes might be used to select the level.
The 0x00000059 and 0x0000005A bytes also seem to be used, but not 100% sure yet.
