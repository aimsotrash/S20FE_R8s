# [Redmi K30 Pro] - [lmi]

Although this device is A-only, you have to choose GSI for A/B devices because this device is "system-as-root". 

## Tested images
√AOSP 10.0 v216

√AOSP 10.0 v217

√AOSP 10.0 v220

√AOSP 11.0 v312

×AndyYan's LineageOS 17.1 20200511 (Doesn't Boot)

×Google GSI, Havoc, CrDroid, LineageOS (Credits Chaptsand from CoolApk, same w/ Xiaomi Mi 10 umi)

√Google GSI(Official Android 12)

## Flashing instructions (Credits phhusson and Akito, make sure to have the latest platform-tools installed)

Reboot to bootloader:
```
adb reboot bootloader
```
Flash vbmeta with 
```
fastboot --disable-verity --disable-verification flash vbmeta vbmeta.img
``` 
If using wzsx150's unofficial TWRP, flash stock recovery
```
fastboot flash recovery recovery.img
```
Reboot to fastbootd
```
fastboot reboot fastboot
```
Flash system with
```
fastboot flash system system.img
```
Wipe data
```
fastboot -w
```
Reboot phone
```
fastboot reboot
```

## Hardware support (Referred from Redmi K20 Pro)

| Component                 |      Comment                                              |
|---------------------------|-----------------------------------------------------------|
| Camera                    | √× (Cameras work, but front camera does not popup at all, please read note 1); Stock camera apk supports main and front camera |
| Audio                     | √ Speaker and microphone is working, USB Type C DAC is working, 3.5mm audio jack is working. |
| Bluetooth                 | √? Bluetooth Speaker works fine, In-call is untested. |
| Display                   | √ |
| WiFi / Hotspot            | √ |
| GPS                       | √ |
| SIM / Mobile Data / Voice | √× Internet Data works, call works, expect messages to be NOT working. |
| VoLTE                     | ? (Untested) |
| LED                       | √? Working, unsure about the second LED [Need more testing]. |
| Fingerprint               | √× (Recognition a little slower maybe due to system setting; Unlocking from off/AOD state not supported, need press power button first, not working since 216+) |
| NFC                       | √? (Support card info reading via NXP.TagInfo, need more tests like card writing / simulation) |
| Offline Charging          | × |

## Additional Note

1. Terminal command for manually controlling the front camera motor (may require `su` depending on the GSI):

Popup: `xiaomi-motor popup 1`

Retract: `xiaomi-motor takeback 1`

2. Disable "audio effects" in phh treble settings to make audio work normally

3. Use the alternative audio strategy in phh treble settings to prevent audio from stopping for a short time randomly.

---

This wiki page is referred from Xiaomi Redmi K20 Pro (raphael) page as this device have a lot of things in common with in.

Redmi K30 Pro Tested By: 
Akito Mizukito (RealAkito) @ Redmi K30 Pro V11.0.6.0.QJKEUXM / V11.0.16.0.QJKCNXM / 20.5.14 Beta 

lulujyc @ 20.5.21 Beta, 12.0.1 Stable (12.0.1 is recommended as it's more stable)

lulujyc @ Android 11 Beta 1: Doesn't boot any GSI including Google's Android 11 sGSI.

EdChdX @ Redmi POCO F2 Pro

asrieldashie @ 2021.10.04 . With PixelExtended vendor

Origin Redmi K20 Pro Wiki is made by AndyYan (AndyCGYan)

Template created by @zguithues and @hackintosh5