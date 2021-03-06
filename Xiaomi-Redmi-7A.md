# Device Info

- Name: Xiaomi Redmi 7A  
- Architecture: arm32_binder64 (a.k.a. a64) and arm64 unofficial @ https://web.telegram.org/#/im?p=@PineOfficial
- System partitions: a-only system partition, but use ab rom
- System-as-root: Yes

## Steps to install
Refer to XDA Thread
https://forum.xda-developers.com/redmi-7a/how-to/custom-gsi-firmware-t3965820

*Some more info*

- Like all Xiaomi's devices, it takes one week to unlock the bootloader.
- If you see insufficient storage when installing gapps resize the system partition on TWRP using the command `resize2fs /dev/block/mmcblk0p57` then try flashing gapps
- If a gsi treble rom does not boot either the rom is not arm 32 binder 64 or your vendor implementation is broken. Try reflashing vendor from MIUI Official Fastboot Rom, links can be found [here](https://mirom.ezbox.idv.tw/en/phone/pine/)
- To root Redmi 7A, patch your boot image by goin to this link https://patcher.yaalex.xyz/ and then flash latest magisk.zip. You may have to manually install magisk manager
- If you want to use 64 bit version or report any bugs try following this telegram link: https://web.telegram.org/#/im?p=@PineOfficial

## Hardware support

| Component                 |      Pie                             |              10                |11
|---------------------------|--------------------------------------|--------------------------------|-----------------------
| Camera                    | Video recording broken after 24 hours| Working from v220 onwards, can be fixed using treble settings from v217 onwards |working|
| Speaker / Mic             | Working                              | Working                       |working|
| Bluetooth                 | Working                              | Working                       |working|
| WiFi                      | Working                              | Working                       |working|
| SIM / Mobile Data / Voice | Working                              | Working                       |working|
| VoLTE                     | Working with [Patch]                 | Working with [Patch]          |not tested, ask on telegram|
| Offline Charging          | Working, hard reboot requried to reach system | Working, hard reboot requried to reach system |same as android 9 and 10|
| Magisk           | Working after [patching boot image](https://patcher.yaalex.tk) | Working after [patching boot image](https://patcher.yaalex.tk)                      | not tested, ask on telegram |
| Root (phh-su) | Working | Working | working |
| Adoptable Storage         | Working                              | Working                       |not tested|
---

additional info:
- fm radio also working in gsis, using magisk module.

- for good performance, i suggest you to use latest [arm64 vendor] and [cherry kernel]

---

Tested By: 
- @KhushrajRathod: VoLTE, Adopted Storage, Camera, Root, Magisk, Offline Charging 
- Ralph Garcia: Other features
- vytska69 and redmi 7a comunity: arm64 with cherry kernel
---

Tested Roms:
- [10] Phhusson's AOSP 10.0 v222
- [10] Havoc Os 3.8
- [10] Bliss os

- [11] LineageOs and PHH roar

Template created by @zguithues and @hackintosh5

[Patch]: https://github.com/KhushrajRathod/VoLTE-Fix
[cherry kernel]: https://androidfilehost.com/?fid=17248734326145738587
[arm64 vendor]: https://drive.google.com/uc?id=1C5d4iDzF94LVHmJ0MWNwIpGPgWX10Y6e&export=download