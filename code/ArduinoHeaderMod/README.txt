This file belongs in <PathToArduinoIn Program Files (x86)>\Arduino\hardware\teensy\avr\cores\teensy3

Changes "Keyboard/Joystick/Mouse" to just be a "Joystick".

Windows is fine, but Linux was seeing two I/O devices and treating them as seperate joysticks.  Worked fine for single player, but a second controller would show up as player 3, instead of 2.

Annoyingly, I also had to chnge the PRODUCT_ID to something Teensy wasn't already using.  Windows caches all data about a USB device and never looks again.  This undesirable behavior means the device can never change.  Down side, Teensy cannot automatically find the device.  Upload will fail, and you will have to push the "reboot" button on the Teensy to load updates.