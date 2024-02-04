# AutoROM

## Description
This repository only has the build of AutoROM project, does not contain code cause the company's policies.

The AutoROM is the project that we will use for install some public ROM we has see on the internet (such as LineageOS). It's support to install ROM for 3 devices, include Samsung Galaxy S9 (starlte), Xiaomi Mi A1 (tissot) and Google Pixel 3A (sargo).
Also some ROMs just have the build, not include Google Services, so I also add install GApps feature for installing to that type of ROM.
Inside this, I also add an option is re-stock device which will bring device ROM come into manufacturing version. 

## Instruction
Example:
With Samsung Galaxy S9, for installing new ROM:
For some reasons, we must bring device to Recovery mode before install new ROM.
* The first one, we must ensure that OEM unlock feature is enabled on device (we can check them on device by Open Settings > About phone > Software information > Make multiple taps into "Build number" until the Developer Options is unlocked > Then back to Settings > select Developer options and we can check OEM unlock here).
* Next, we reboot device into Download mode.
* In here, we flash a software called "TWRP" into device By Odin3 application
* Then the TWRP is flashed, the device is auto reboot, now we must hold the Volume Up + Bixby + Power buttons until the TWRP shows on the screen.
* Finally, open tools, load the devices, pick a ROM and Gapps (if needed) and then select what devices we want to install. The tools will auto do something else to install new ROM later.

## Resources
* Android SDK (ADB + Fastboot): https://developer.android.com/tools/releases/platform-tools?hl=en (Download based on your OS version).
* TWRP
1. S9: https://dl.twrp.me/starlte/ (use .tar file)
2. A1: https://dl.twrp.me/tissot/
3. 3A: https://dl.twrp.me/sargo/
(With A1 and 3A don't need to boot into Download mode, they have a mode called Fastboot, we just boot them into Fastboot, and then use the AutoROM to flash them to TWRP, the AutoROM will find inside the directory 2 files, once is recovery_tissot.img (represents for TWRP of Xiaomi A1) and second one is recovery_sargo.img (respresents for Pixel 3A), so we must download 2 TWRP files and copy them into AutoROM's directory and rename them to recovery_tissot.img and recovery_sargo.img).
* With the stock ROM feature, we must need download and copy the stock ROM files into folder <AutoROM directory>/Resources/stock_firmware/... (copy based on device stock firmware file).

Thanks for reading!