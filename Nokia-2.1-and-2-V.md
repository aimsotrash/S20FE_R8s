# [Nokia 2.1 / V] - [e2m / evw]

## Hardware Support (AOSP 8.1)

| Component                 |      Comment                                              |
|---------------------------|-----------------------------------------------------------|
| Camera                    | √                                                         |
| Speaker / Mic             | √                                                         |
| Bluetooth                 | √                                                         |
| WiFi                      | √                                                         |
| SIM / Mobile Data / Voice | √                                                         |
| VoLTE                     | √                                                         |

Night Light doesn't work on this build.

## Hardware Support (AOSP 9)

Boot failed.

## Hardware Support (AOSP 10)

| Component                 |      Comment                                              |
|---------------------------|-----------------------------------------------------------|
| Camera                    | √                                                         |
| Speaker / Mic             | √                                                         |
| Bluetooth                 | √                                                         |
| WiFi                      | √                                                         |
| SIM / Mobile Data / Voice | √                                                         |
| VoLTE                     | √                                                         |

Possibly due to hardware video decoding broken, the navigation key option can't be accessed without workaround.

Here's the workaround (AOSP 10 V203):

Download rw-system.sh you'll need to replace from here : https://github.com/phhusson/device_phh_treble/blob/android-10.0/rw-system.sh

`adb root & adb remount & adb push rw-system.sh /system/bin/rw-system.sh`

## Hardware Support (AOSP 11)

| Component                 |      Comment                                              |
|---------------------------|-----------------------------------------------------------|
| Camera                    | √                                                         |
| Speaker / Mic             | √                                                         |
| Bluetooth                 | √                                                         |
| WiFi                      | √                                                         |
| SIM / Mobile Data / Voice | √                                                         |
| VoLTE                     | √                                                         |

Possibly due to hardware video decoding broken, the navigation key option can't be accessed without workaround. Workaround for AOSP 10 doesn't work for AOSP 11 build.

***
## Additional Notes

For AOSP 8.1, "arm-aonly-go" flavor is known working.

For AOSP 9, since there's no "arm-ab-vanilla" flavor, you have to use Android 8.1 stock vendor along with "arm-aonly-vanilla" flavor, but it gets stuck at "Android" animation forever.

For AOSP 10, "arm-ab-vanilla" flavor is known working.

For AOSP 11, "arm-ab-vanilla" flavor is known working.

If no navigation bar during boot, you must use following command under root permission to add it:

`setprop persist.sys.phh.mainkeys 0`

***


## Tested By:

AOSP 8.1 on E2M: * Calyx Hikari (HikariCalyx) @ Nokia 2.1 00WW_0_390 @ 09/11/2019

AOSP 9 on E2M: * Calyx Hikari (HikariCalyx) @ Nokia 2.1 00WW_0_390 @ 08/11/2019

AOSP 10 on E2M: * Calyx Hikari (HikariCalyx) @ Nokia 2.1 00WW_1_13F @ 08/11/2019

AOSP 11 on E2M: * Calyx Hikari (HikariCalyx) @ Nokia 2.1 00WW_4_11F @ 29/01/2021


Template created by @zguithues