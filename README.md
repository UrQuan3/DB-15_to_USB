# DB-15_to_USB
Use of Teensy microcontrollers for use with SNK/SuperGun style fightsticks.

This repository contains the source code for the DB-15_to_USB board I designed, though it would be very easy to adapt to other projects.  I had made several DB-15 fightsticks for use with the DB-15_to_JVS project, but also wanted to use them on normal PCs.  This is a very simple project.

This adapter has been tested and functions in:
- Windows 10 (DirectInput)
- Linux
- Raspbian
- Retropie
- EmuELEC

This does not support the Microsoft proprietary XInput and is unlikely to support any game consoles with USB inputs.

This code does not implement SOCD (Simultaneous Opposite Cardinal Directions) cleaning.  It would be easy to add, but I prefer zeroing the output and lighting a warning light for debugging hand built controllers.

Setup instructions:
- Install the arduino software and the Teensy libraries:
https://www.arduino.cc/
https://www.pjrc.com/teensy/td_download.html
- Open this project in the arduino software
- Under "Tools->Board", set your board type.
- Under "Tools->USB Type", pick something that includes "Joystick"

Known bugs:
- Like all USB HID devices, attaching two identical devices will work, but on each startup they will be assigned an order at random.  The host system cannot tell them apart and therefore does not know which one you want to be "Player 1".



