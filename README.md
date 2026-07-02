# Metz Mecablitz/Mecalight Firmware Updater and DFU Files

This is the original firmware updater for the following Metz models:
- Mecablitz M360
- Mecablitz M400
- Mecablitz 64 AF-1
- Mecalight L1000

The updater for many other models is still downloadable from other sources, and these updaters include the corresponding *.mtz firmware file. For the models M360, M400, 64 AF-1, and L1000, Metz changed the updater so that it no longer includes the firmware file and instead downloads the firmware as a *.dfu file from their server. Surprisingly, this still seems to work as of May 2026, but the server will likely be taken offline at some point in the future. That is why I created this repository. It contains all the *.dfu files that I could find. When the server is taken offline and the updater becomes useless, these files can still be installed using the `dfu-util` CLI that comes with the updater.

The firmware files are currently (May 2026) still hosted on `https://metz.de` and you can download them yourself via `https://metz.de/firmware/<filename>` (find file names below).

When using the updater, *.dfu files are downloaded to `C:\Users\<username>\AppData\Local\Metz mecatech GmbH\mecablitz Firmware Updater\mecatech\..` but the updater doesn't seem to use already existing *.dfu files in that directory.

# Files

- MB3600b0.dfu - M360 Canon 
- MB3600b1.dfu - M360 Nikon 
- MB3600b2.dfu - M360 Olympus 
- MB3600b4.dfu - M360 Sony 
- MB3600b6.dfu - M360 Fuji 
- MB400190.dfu - M400 Canon 
- MB400191.dfu - M400 Nikon 
- MB400192.dfu - M400 Olympus 
- MB400193.dfu - M400 Pentax 
- MB400194.dfu - M400 Sony 
- MB400196.dfu - M400 Fuji 
- MB640170.dfu - 64AF-1 Canon 
- MB640171.dfu - 64AF-1 Nikon 
- MB640172.dfu - 64AF-1 Olympus 
- MB640173.dfu - 64AF-1 Pentax 
- MB640174.dfu - 64AF-1 Sony 
- MB1001a0.dfu - L1000

# Instructions

As of May 2026, all you need to update your flash is `mecablitzinstall.exe`. This executable will extract the updater to `C:\mecablitz` by default. From there, simply run `mecablitz.exe` and follow the instructions.

When the server hosting the *.dfu files is taken offline, this updater will no longer work. In that case, you can install the update by using the `dfu-util` CLI (`C:\mecablitz\dfu-util\dfu-util.exe`) and the *.dfu file from this repository that corresponds to your flash model. 

# Additional Content

This repository also contains the latest updater (V6.0) for the Pentax versions of the 44 AF-1, 48 AF-1, 50 AF-1, 58 AF-1, and 58 AF-2. This version adds support for the Pentax K1.

This might be the last remaining reliable source of this particular updater.
