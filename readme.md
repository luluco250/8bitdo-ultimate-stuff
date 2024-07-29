## 8BitDo Ultimate Controller Stuff

This repository contains random stuff I've collected related to 8BitDo's Ultimate controller.

Specifically the beta firmware is actually better for Linux since it allows explicit input mode selection through shortcuts similar to their pre-Pro 2 controllers:

You can use a Windows virtual machine to flash the firmware, note that you will need to passthrough the USB receiver, not the controller.
You also need to passthrough a new boot mode device that shows up when you start the firmware update process.

To select an input mode, hold one of these combos while the controller is off:
```
+--------------+---------+ +--------+-------+--------+
|    Combo     |  Mode   | | Layout | Xbox  | Switch |
+--------------+---------+ +--------+-------+--------+
| Guide+West   | XInput  | | Guide  | Guide |  Home  |
+--------------+---------+ +--------+-------+--------+
| Guide+East   | DInput  | | West   |   X   |   Y    |
+--------------+---------+ +--------+-------+--------+
| Guide+North  | Switch  | | East   |   B   |   A    |
+--------------+---------+ +--------+-------+--------+
| Guide+South  | Apple   | | North  |   Y   |   X    |
+--------------+---------+ +--------+-------+--------+
                           | South  |   A   |   B    |
                           +--------+-------+--------+
```
No license is available because it's 8BitDo's copyright, this repository is offered for the purpose of archival and allowing better use of the controller on Linux.
