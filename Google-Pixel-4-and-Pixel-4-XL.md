**Device:** Pixel 4 XL

**Summary:** I tested the quack vanilla versions until v213. Mostly everything works (wlan, mobile connection, camera etc) and the rom is very stable on this phone. Nevertheless the wlan connection isn't so stable even with full signal strength. 
I can't say anything about bugs in the gapps version for this phone because i don't use these builds.


**Steps to install:**

   Step 1: Download the quack vanilla build and the vbmeta from phh

   Step 2: Boot the phone into fastboot mode (over hardware buttons or adb)
    
   Step 3: Flash the vbmeta.img. 
           _Command:_ `flash vbmeta vbmeta.img`

   Step 4: Boot into fastbootd mode.
           _Command:_ `fastboot reboot fastboot`

   Step 5: Erase the current system.
           _Command:_ `fastboot erase system`

   Step 6: Flash the build of phh quack.
           _Command:_ `flash system "Name of the build".img`

   Step 7: Erase userdata.
           _Command:_ `fastboot -w`

   Step 8: Reboot the phone
          _Command:_ `fastboot reboot`


**Hardware support:**

* Camera: Works
* Speaker / Mic: Works
* Bluetooth: Works
* WiFi: Works (but not completly stable)
* SIM / Mobile Data / Voice: Works
* VoLTE: Not tested 
* Fingerprint: Not tested
* NFC: Works
* Offline Charging: Not tested
* NFC: Works
* Storage connection to PC: Works