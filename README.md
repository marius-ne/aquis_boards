# aquis_boards
Arduino definition files for the SpaceTeamAachen Aquis microcontrollers.

## package_aquis_index.json
I added a workaround because the internal package_index.json that is shipped with the Arduino IDE uses an out-of-date version of the openocd tool. You can see it under the "tools" section. It just uses the up-to-date version of the one used by the Adafruit SAMD package index.

## Installing

You first <b>have to</b> install the "Arduino SAMD" package from the boards manager, this is strictly required.

Add the json location (https://raw.githubusercontent.com/marius-ne/aquis_boards/master/package_aquis_index.json) in the preferences (section "additional board managers URL") of the Arduino IDE. Then install it via searching for "Aquis" in the board manager. You will see a red error appear in the console that says something about a non trusted contribution. You can ignore this.

## Version guide

- 1.0: contains an exact copy of the trinket m0 variant.cpp and variant.h files. Is used for testing the implementation into the Arduino IDE.
- 1.1: contains an edited version of the trinket m0 variant files to try out changing the mapping of the pins (switching A1 and A2).

## How to create new version

- 1.: copy previous folder version and make desired edits in variant files.
- 2.: edit version number in platform.txt.
- 3.: create zip file and invoke CRC-256.
- 4.: create new version in package index.
- 5.: copy CRC and size into package index.
- 6.: git add, commit and push into repo.
- 7.: update README.
