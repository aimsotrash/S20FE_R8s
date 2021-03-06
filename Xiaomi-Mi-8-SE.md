# Xiaomi Mi 8 SE AOSP ROM (GSI Treble based) installation guide - Vanilla Android experience
## Discussion on XDA
https://forum.xda-developers.com/mi-8-se/how-to/comprehensive-guide-installing-aosp-gsi-t3930100/
## Hardware support

Known issues https://github.com/phhusson/treble_experimentations/issues/398

| Component                 |      Comment                                              |
|---------------------------|-----------------------------------------------------------|
| Camera                     | Working (auxiliary camera can be detected by Open Camera, however can't be used with apps other than MIUI stock camera. Front/rear flashlight working)                                                   |
| Speaker / Mic             | Working                                                   |
| Bluetooth media           | Working                                                   |
| Bluetooth in-call/outgoing-call         | Not Working, also presents in other devices using GSI                                              |
| WiFi                      | Working                                                   |
| Dual SIM / Mobile Data (LTE) / Voice (GSM)| Working                                                   |
| VoLTE                     | Not working Needs someone with knowledge in Android development working on this https://github.com/phhusson/treble_experimentations/issues/398#issuecomment-469669971                                             |
| Fingerprint               | Working                                                   |
| Offline Charging          | Working                                                    |
| IR             | Working                                                    |


## The guide guy
This guide should also apply to any other recent Xiaomi phone with fastboot support.

This is an A-only device without Xiaomi's newly introduced anti-rowback (downgrade) mechanism. Originally shipped with Android 8.0 in June 2018. Supports dual-SIM VoLTE on stock firmware with Snapdragon SDM 710 SoC. available in 4/64, 6/64, 6/128.
GSI images relies on the stock vendor partition to work properly. So stick to the GSI image with the same Android version as the MIUI. At this moment, May 2019, Xiaomi has released pie based firmware for this device.
In the future, if you want to upgrade the system of your phone, the whole procedure described on this page will need to be performed again to avoid problems. (And search for the TWRP works with future release, in case the one on this page is outdated)
Before you do anything, please BACK UP YOUR FILES!!!

### Required files
-1. A Windows 7 or later computer with at least 10 GB free space

0. Official bootloader unlocker http://miuirom.xiaomi.com/rom/u1106245679/3.3.1212.33/miflash_unlock-3.3.1212.33.zip
1. Stock fastboot mode latest stable firmware http://update.miui.com/updates/v1/fullromdownload.php?d=sirius&b=X&r=cn&n= . With this, you can go back to stock at anytime if something goes wrong.
2. Stock fastboot mode firmware flashing tool http://bigota.d.miui.com/tools/MiFlash2018-5-28-0.zip
3. LR.team 2019-04-23 unofficial TWRP 3.3.0 (data partition decryption seems not working )with flashing tool https://mailacid-my.sharepoint.com/:u:/g/personal/tsh_mail_ac_id/EXVUGoX4qLlDiXms2ZJDCG0BfZWRfvp5rwNVHavhsz9IYw?e=TgYdHk
4. Latest stable xiaomi.eu ROM. Same version as the downloaded stock firmware recommended. https://sourceforge.net/projects/xiaomi-eu-multilang-miui-roms/files/xiaomi.eu/MIUI-STABLE-RELEASES

Tested combination:

Xiaomi EU ROM
https://kent.dl.sourceforge.net/project/xiaomi-eu-multilang-miui-roms/xiaomi.eu/MIUI-STABLE-RELEASES/MIUIv10/xiaomi.eu_multi_MI8SE_V10.3.1.0.PEBCNXM_v10-9.zip 

Stock MIUI fastboot image 
http://bigota.d.miui.com/V10.3.1.0.PEBCNXM/sirius_images_V10.3.1.0.PEBCNXM_20190418.0000.00_9.0_cn_77c3bfb3d6.tgz

5. phhson generic AOSP system image for arm64 A-only devices https://github.com/phhusson/treble_experimentations/releases
6. Following procedure is executed under Windows
7. FOSS compressed archive tool https://www.7-zip.org
### 0. Unlock bootloader and flash the latest stock MIUI firmware in fastboot mode 
1. Unlock the bootloader here http://en.miui.com/unlock/ (wipe all existing data) and put it in fastboot mode after unlock. (Power it off first, then power it on while holding volume down button.)
2. Extract the firmware and the flashing tool.
3. Run MiFlash.exe in the tool's folder. Install drivers by clicking Drivers in menu bar.
4. Select the firmware folder and click load to detect fastboot mode devices.
5. Select a flash method without "lock" in the low right corner of the flashing tool interface. Default option will lock the bootloader!!!
6. Flash the ROM and wait it to reboot into MIUI welcome screen.
### a. Installing TWRP recovery 3.3.0 on Xiaomi MI 8 SE
1. Extract the downloaded file.
2. Run recovery-twrp-one-click-flashing-tool????????????.bat
3. Follow the instructions on screen
4. Change language to English after first boot by following means.
1. Slide the button to allow modification
2. Tap "??????", third line second row.
3. Tap the globe tab on the right side
4. Select English and tap language button on the low right corner

> Tip: If TWRP does not start then use combination of buttons `(POWER) + (VOLUME +)` to force the device to start from the recovery 

### b. Installing the latest available version of MIUI EU (or flash the boot.img only)
1. Enter `TWRP` and perform `WIPE > FORMAT DATA` and `FACTORY RESET`
2. Copy the ZIP file (MIUI 10) to `DEVICE / TWRP` from the `Windows Explorer` (Drag and Drop)
3. Next go to `INSTALL > INSTALL ZIP`, enter the directory `/data/media/0/TWRP`, flash ZIP file and finish by pressing `SWIPE TO CONFIRM FLASH`
4. Wait for the installation to finish (the system starts in initial MIUI screen)

Alternatively you can just extract the boot.img file from xiaomi.EU ROM zip file and flash it as the description of AOSP system image flashing.

> Note: Actually this step replaces stock boot.IMG with the one from xiaomi.eu, Since GSI image doesn't boot with the stock one. And if the xiaomi.EU version doesn't match with the stock MIUI version on device (I.e. boot.IMG doesn't match other blobs), the device will kick into fastboot to force you to perform a fresh installaion of stock MIUI, or exhibiting unforseeable problems eg. touchscreen not working.

### c. Installing GSI AOSP system image
1. Download the latest version of the GSI
2. Extract the contents of the `.xz` file with 7-zip download [here](https://www.7-zip.org/) 
3. Enter `TWRP` and perform `WIPE > SWIPE TO FACTORY RESET`
4. Copy the IMG file (GSI AOSP) to `DEVICE / TWRP` from the `Windows Explorer` (Drag and Drop)
5. Next go to `INSTALL > IMAGES`, enter the directory `/data/media/0/TWRP`, flash file `IMG` then select partition `SYSTEM` and finish by pressing `SWIPE TO CONFIRM FLASH`
6. Restart to `SYSTEM` (Normal restart)
7. Wait for the installation to finish and the system will start the initial screen of `AOSP 9 PIE`
![](https://user-images.githubusercontent.com/47562939/57715499-7cfcbe80-76a9-11e9-9ad3-9d8ae7095dfd.png)
![](https://user-images.githubusercontent.com/47562939/57715509-8423cc80-76a9-11e9-97d1-783fe5bcc5a9.png)
tested by dkmgfk May 2019

### Template created by @alonsok28