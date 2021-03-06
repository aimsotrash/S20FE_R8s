# Moto G5

Not suitable for daily usage.

## Steps to install

### Clean flash
* Flash [this TWRP](https://drive.google.com/open?id=1XqpR6vYEbSXKZFD7StXc69jsh6YAOr3m) as "Recovery" in your existing recovery.
* Reboot again to TWRP.
* Format System, Data, Cache and Dalvik/ART Cache.
* Flash [this ROM](https://drive.google.com/a/al.educacao.sp.gov.br/uc?id=1onmjOKJAPFeiws8MXTyeMGwIIF6gguYj&export=download).

**Optional:**
* Reboot to TWRP.
* Format System.
* Flash a GSI as "System Image". Or alternatively use fastboot to flash the GSI:
```
fastboot flash system path/to/gsi.img
```
* Reboot to system.

### Dirty flash

**Whole system:**
* Reboot to TWRP.
* Flash the latest LineageOS Treble zip.
* Format system and reinstall your GSI.
* Reboot to system.

### Android 10
* Follow the clean flashing steps. Do **not** reboot.
* Flash [this](https://github.com/montanadevelopment/releases/releases/download/Android10Fixes-1/allzygotefix2.zip), then [this](https://github.com/montanadevelopment/releases/releases/download/Android10Fixes-1/lagfix-for-a_and_ab.zip) and then [this](https://github.com/montanadevelopment/releases/releases/download/Android10Fixes-1/Q-google-debloat.zip).
* Reboot to system.

[Some more info](https://t.me/g5treble)

### Android 11
* Follow the clean flashing steps. Reboot to system and let LineageOS boot.
* Reboot to TWRP Recovery
* Flash GSI img as system
* Reboot system

## Hardware support

| Component                 |      Comment                                              |
|---------------------------|-----------------------------------------------------------|
| Camera                    | Front cam is buggy, video recording broken                |
| Speaker / Mic             | Working                                                   |
| Bluetooth                 | Working                                                   |
| WiFi                      | Working                                                   |
| SIM / Mobile Data / Voice | Working                                                   |
| VoLTE                     | Not Working                                               |
| Fingerprint               | Working                                                   |
| Offline Charging          | Working                                                   |
| Other feature             | -                                                         |

## Hardware support on Android 11 ARM64

| Component                 |      Comment                                              |
|---------------------------|-----------------------------------------------------------|
| Camera                    | Not working (lack of drivers, maybe?)                     |
| Speaker / Mic             | Working                                                   |
| Bluetooth                 | Working                                                   |
| WiFi                      | Working                                                   |
| SIM / Mobile Data / Voice | Unknown                                                   |
| VoLTE                     | Unknown                                                   |
| Fingerprint               | Working                                                   |
| Offline Charging          | Working                                                   |
| Other feature             | -                                                         |


## GSI support

<details><summary>Booting:</summary>
<p>

[AOSP 11.0 v300.g](https://github.com/phhusson/treble_experimentations/releases/tag/v300.g)

</p>
</details>

<details><summary>Not Booting:</summary>
<p>

TBD
</p>
</details>

---

Tested By: Brickador - XT1672 (Brazil), Firmware Version: Oreo B831, Date tested: TBD

Also tested by: ludke (SludkeSP)

Android 11 tested by: xatornet - XT1676

Template created by @zguithues and @hackintosh5