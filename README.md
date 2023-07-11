# Marlin-H32

Just forking [alexqzd/Marlin-H32](https://github.com/alexqzd/Marlin-H32) to fix my probing issues using a Creality CR-Touch probe on a Voxelab Aquila X2 using this [CR-Touch mount by LightValen](https://www.thingiverse.com/thing:4974329) with the stock shroud. The default probing margin was set to a value of 20, which is changed to 30 in order prevent the X-axis bumping into the right frame.

## Flashing Aquila X2 with H32 board

* Format a SD card as FAT32 with a cluster size of 4096 bytes.
* Download [Alex' Marlin source code](https://github.com/alexqzd/Marlin-H32/archive/refs/tags/v1.3.6.zip) for the screen assets.
* In the source code archive, copy the Copy the `DWIN\_SET (Voxelab Red)` folder to the root your formatted SD card. Rename the folder back to only `DWIN\_SET`.
* Download one of the [precompiled binaries on the release page](https://github.com/vuhuy/Marlin-H32/releases/) for the firmware upgrade. I've chosen `BLTouch-9x9-H32.bin` (also works for CR-Touch, 9x9 for 81 probing points, non high-speed HS).
* Create a folder on the SD card root named `firmware` and copy the download BIN file into that folder.
* Make sure your Aquila X2 is turned off, insert the prepared SD card into the printer base and turn the machine on.
* It will start to flash firmware immediately. If it's booting into normal operation mode, your SD card is not prepared correctly. It will show a broken progress bar and come back alive after while. The screen might show mangled graphics when flashing is done.
* Turn off the machine to flash the display assets. Remove the SD card, disconnect and dismount the screen from the printer base.
* Unscrew the back cover from the screen to access a hidden SD card reader. You don't have to remove the mount from the display module. Insert the SD card, and reconnect the screen. It's better to not reassembly the whole thing at this point.
* Start your machine. If your SD card is prepared correctly, you will be greeted with a blue screen. When flashing the screen assets is done, the screen will flash orange.
* Turn off the machine, remove the SD card, and turn on the machine to verify the printer is working correctly. Reassemble the printer if everything works fine.