# Tested Image:  AOSP 10.0 v222

## Functions

Camera : Work (Only center lens)

Speaker / Mic : Work(Need to enable "Use alternate audio policy" and "Disable audio effects" in Settings -> "Phh Treble Settings")

Bluetooth : Work

WiFi : Work

SIM : Work(May need fix for some certain carriers such as ChinaUnicom and ChinaTelecom to solve SMS/MMS problems. I recommend to just flash [this](https://github.com/KhushrajRathod/VoLTE-Fix))

VoLTE : Work

Fingerprint : Work

NFC : Work

Offline Charging : Not tested

5G : Not tested

***

# Tested Image:  AOSP 11.0 v300.l

## Functions

Camera : Work (Only center lens)

Speaker / Mic : Work(Need to enable "Use alternate audio policy" and "Disable audio effects" in Settings -> "Phh Treble Settings")

Bluetooth : Work

WiFi : Work

SIM : Work(Instead of flashing fix-patch manually, just use "Install IMS APK for Qualcomm vendor" in Settings -> "Phh Treble Settings" -> "IMS Features")

VoLTE : Not working

Fingerprint : Not working(The system thinks the fingerprint sensor is on the back)

NFC : Not tested

Offline Charging : Not tested

5G : Not tested

*Note: If you do a straight update from Android 10, the system's Package Installer may be broken. Either choose a factory reset after flashing or SAI from Play Store as an alternative installer.


***

Tested By Sosueyakiko

Based on MIUI China 12.0.5(Stable)
