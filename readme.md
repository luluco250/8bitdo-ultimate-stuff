## 8BitDo Ultimate Controller Stuff

This repository contains random stuff I've collected related to 8BitDo's Ultimate controller.

Specifically the beta firmware is actually better for Linux since it allows explicit input mode selection through shortcuts similar to their pre-Pro 2 controllers:

You can use a Windows virtual machine to flash the firmware, note that you will need to passthrough the USB receiver, not the controller.
You also need to passthrough a new boot mode device that shows up when you start the firmware update process.

To select an input mode, hold one of these combos within 5 seconds after turning the controller on:
```
+----------------+--------+ +--------+-------+--------+
| Combo          | Mode   | | Layout | Xbox  | Switch |
+----------------+--------+ +--------+-------+--------+
| Select + North | XInput | | Select | Back  | -      |
+----------------+--------+ +--------+-------+--------+
| Select + South | DInput | | Start  | Start | +      |
+----------------+--------+ +--------+-------+--------+
| Select + West  | Switch | | North  | Y     | X      |
+----------------+--------+ +--------+-------+--------+
| Start + Select | Auto   | | South  | A     | B      |
+----------------+--------+ +--------+-------+--------+
                            | West   | X     | Y      |
                            +--------+-------+--------+
```
No license is available because it's 8BitDo's copyright, this repository is offered for the purpose of archival and allowing better use of the controller on Linux and no copyright violation is intended.

This means no warranty is provided and you're on your own if your controller breaks, do not hold the maintainer(s) of this repository or 8BitDo liable for any damages caused by its use.
