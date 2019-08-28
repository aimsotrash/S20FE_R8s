# Asus Zenfone Live L1 (ZA550KL)
![Asus Zenfone Live L1 (ZA550KL)](https://cdn2.gsmarena.com/vv/pics/asus/asus-zenfone-live-l1-za550kl-2.jpg)

Asus Zenfone Live L1 (ZA550KL) codenamed "ASUS_X00RD" is a budget smartphone from ASUSTeK Computer Inc. released in May 2018.

## DEVICE SPECIFICATIONS
|      Feature      |                         Information                          |
|-------------------|--------------------------------------------------------------|
| Dimensions        | 147.3 x 71.8 x 8.2 mm (5.80 x 2.83 x 0.32 in)                |
| Network Standard  | FDD-LTE, TDD-LTE, WCDMA, GSM                                 |
| SIM Cards         | Dual SIM & one microSD card                                  |
| CPU               | Qualcomm® Snapdragon™ 425 Mobile Platform with 28nm, 64-bit Quad-core Processor |
| GPU               | Qualcomm® Adreno™ 308                                        |
| Memory            | LPDDR3 2GB / 3GB                                             |
| Internal Storage  | eMCP 16 / 32 GB                                              |
| MicroSD card      | Supports up to 2 TB                                          |
| Battery           | 3000mAh capacity                                             |
| Display           | 5.5-inch 18:9 HD+ (1440 by 720) IPS display                  |
| Rear Camera       | 13MP, F2.0 aperture, Phase-detection autofocus, LED flash    |
| Front Camera      | 5MP, F2.4 aperture, Softlight LED flash                      |
| Wireless Technology     | Wi-Fi 802.11 b/g/n 2.4GHz, Bluetooth 4.0, Wi-Fi direct       |
| Navigation        | GPS, AGPS, GLO, BDS                                          |
| Sensor            | Accelerator, E-Compass, Gyroscope, Proximity sensor, Ambient light sensor        |
| Operating System  | Android™ Oreo™ with new ASUS ZenUI 5                         |

## CONCLUSION
The front and rear cameras work well but with lots of bugs. Flashlight on AOSP / stock camera if set to on or auto the camera will close forcibly. Also the camera has problems taking photos and videos with dark results on some GSI. If we use the front camera, we will see our faces become very strange. Video calls like the WhatsApp application also cannot use the front camera.

## TESTED GSI-TREBLE ROMS
Android 8.1 Oreo list:
* AOSP by Phhusson
* LineageOS by Phhusson
* Official dotOS by dotOS Team
* AICP-mordiford by AndroPlus
* Resurrection Remix by Phhusson
* Bootleggers by Phhusson
* XenonHD by yshalsager
* CrDroid by Dil3mm4

Android 9 Pie list:
* AOSP by Phhusson
* AOSiP by Akhil Narang
* POSP by NFound
* dotOS by NFound
* Official Resurrection Remix by mracar
* Official AEX by EnesSastim
* Official HavocOS by vince31fr
* Descendant by Dil3mm4
* LineageOS by AndyYan
* Pixel Experience by EnesSastim
* OctopusOS by Deepflex

## STEPS TO INSTALL
1. Extract the compressed zip or xz file to retrieve the img file.
2. Boot your device into fastboot mode by pressing the volume up and power buttons simultaneously.
3. Flash the image file into the system image partition with fastboot command with this command : `fastboot flash system system-image-filename.img`

## HARDWARE SUPPORT
|         Component         |                         Comment                      |
|---------------------------|------------------------------------------------------|
| Camera                    | Working (with bugs, dark)                            |
| Speaker / Mic             | Working                                              |
| Bluetooth                 | Working                                              |
| WiFi                      | Working                                              |
| SIM / Mobile Data / Voice | Working                                              |
| VoLTE                     | Not working (but can be fully functional with a patch)      |
| Hotspot                   | Working                                              |
| Flashlight                | Working                                              |
| Offline Charging          | Working                                              |
| Other feature             | I haven't tried all the features yet :p              |

## TOOLS & PATCH FIXES:
* [Unofficial TWRP 3.2.3-0](https://www.androidfilehost.com/?fid=6006931924117936924)
* [Decrypt](https://www.androidfilehost.com/?fid=6006931924117940566). Decrypt `/data` partition, so TWRP can read internal storage.
* [Bootloop Patch](https://www.androidfilehost.com/?fid=6006931924117940568). Needed for Android Pie GSI to boot.
* [VoLTE for GSI](https://www.androidfilehost.com/?fid=6006931924117940565). Flash it to get VoLTE feature on GSI.

## TESTED BY:
1. AcAciA
2. Nur Samsu (Samsu Mbilung)
3. [Maulana Kurniawan](https://t.me/maulaaana)
4. [Satu Prasetyo Gilang Mahameru](https://t.me/m4h4m3ru)
5. [Alfian Dwi Affandi](https://t.me/Alfiannnnnnn)
6. [Muhammad Luthfi Taqwim](https://t.me/Iluth_taqwim)
7. And all of [Asus Zenfone Live L1 Indonesia](https://t.me/ZenfoneLiveL1) families ;)