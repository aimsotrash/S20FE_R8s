# [OnePlus Nord N10 5G] - [billie]

This device uses A/B Partition

## Tested image
√AOSP 11.0 v309

_**Prerequisites**_
* OnePlus Nord N10 5G with unlocked bootloader and default recovery
* Latest platform-tools installed `https://developer.android.com/studio/releases/platform-tools`
* Download This Vbmeta `https://dl.google.com/developers/android/qt/images/gsi/vbmeta.img`
* Latest Oxygen update `https://www.oneplus.com/support/softwareupgrade/details?code=PM1605857280263`
* Payloader dumper to extract img files from update `https://github.com/vm03/payload_dumper`**(This will allow you to get the boot.img, modem.img, vbmeta_system.img, and vendor.img)**


_**Steps to Install**_

**1. Reboot to fastboot**
`adb reboot bootloader`

**2. Reboot to fastbootd**
`fastboot reboot fastboot` **(This will show a screen with English at the bottom. This is the correct screen)**

**3. Flash modem_a**
`fastboot flash modem_a modem.img`

**4. Flash modem_b**
`fastboot flash modem_b modem.img`

**5. Flash boot_a**
`fastboot flash boot_a boot.img`

**6. Flash boot_b**
`fastboot flash boot_b boot.img`

**7. Flash system_a**
`fastboot flash system_a system.img`

**8. Flash system_b**
`fastboot flash system_b system.img`

**8.5. _If it says There isn't enough space do these commands_**
` fastboot delete-logical-partition product`, `fastboot delete-logical-partition product_a`, `fastboot delete-logical-partition product_b`, Afterwards run commands 7 and 8 again

**9. Disable verity on vbmeta**
`fastboot --disable-verity flash vbmeta vbmeta.img`

**10. Disable verity on vbmeta system**
`fastboot --disable-verity flash vbmeta_system vbmeta_system.img`

**11. Flash vendor**
`fastboot flash vendor vendor.img`

**12. Wipe Data**
`fastboot -w`

**13. Reboot to system**
`fastboot reboot`

### **_Hardware Support_**
| Component                 |      Comment                                              |
|---------------------------|-----------------------------------------------------------|
| Camera                    | √ Stock camera apk supports main and front camera |
| Audio                     | √? Speaker and microphone is working, USB DAC untested. To enable 3.5mm go into Phh Treble Settings, Qualcomm features, and Use alternative audio policy|
| Bluetooth                 | √ Bluetooth connects fine to enable bluetooth headset go into Settings, Phh Treble Settings, Misc Features and Force-disable A2DP offload|
| Display                   | √ 90hz works fine. Have to go into Settings, Phh Treble Settings, Misc Features, Force FPS, and choose 1080x2400@90.0|
| WiFi / Hotspot            | √|
| GPS                       | √ |
| SIM / Mobile Data / Voice | √ |
| VoLTE                     | √ To enabled it go into Settings, Phh Treble Settings, IMS features,Install IMS APK for Qualcomm vendor, Reboot the device, Go back to IMS features and request IMS network, and Create IMS APN |
| Fingerprint               | √ |
| NFC                       | √ |
| Offline Charging          | √ |

Device tested by:
Coaleb2

Template created by @zguithues and @hackintosh5