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

The controller has a bug where it disconnects if it doesn't receive some ping/pong packets that Linux doesn't send by default unlike Windows and the Switch, so it turns off very quickly after it's not in active use (a game reading inputs for example).

One trick to overcome this, specially when trying to switch input modes, is to forcibly read out the controller constantly.
You can try this shell command to do this (just make sure no other controller is connected first or you'll need to find which `jsX` device is the one used by the controller):
```sh
while :; do
    cat /dev/input/js0 >/dev/null 2>&1
done
```

## Copyright/legal

No license is available because it's 8BitDo's copyright, this repository is offered for the purpose of archival and allowing better use of the controller on Linux and no copyright violation is intended.

This means no warranty is provided and you're on your own if your controller breaks, do not hold the maintainer(s) of this repository or 8BitDo liable for any damages caused by its use.
