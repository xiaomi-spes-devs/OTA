# LineageOS Downloads

### Requirements
The latest Android 16 firmware, an [unlocked bootloader](https://github.com/TheAirBlow/HyperSploit) and USB debugging enabled from developer options.

The latest LineageOS .zip package and boot, KSU_boot, super_empty and vendor_boot .img files for spes available [here](https://github.com/xiaomi-spes-devs/OTA/releases).

The latest version of [Google's platform-tools](https://developer.android.com/tools/releases/platform-tools?hl=en#downloads) and a computer.

If you want to install KernelSU for root, flash the KSU_boot.img from the same release page instead of the regular boot.img, and install the KernelSU APK from that release as well.

### First flash steps
Reboot to bootloader
```
adb reboot bootloader
```

Flash Boot Image
```
fastboot flash boot boot.img
```

If you want KernelSU root instead of the stock boot image, flash the KSU boot image from the release page:
```
fastboot flash boot KSU_boot.img
```
Then install the KernelSU APK from the same release page on your device.

Flash LineageOS recovery
```
fastboot flash vendor_boot vendor_boot.img
```

Reboot to recovery
```
fastboot reboot recovery
```

Do a factory reset (Factory Reset > Format data / factory reset)

Sideload the LineageOS .zip package (Apply Update -> Apply from ADB)
```
adb sideload lineage-packagename.zip
```

Reboot to System

### Manually updating from recovery
Reboot to recovery
```
adb reboot recovery
```

Sideload the LineageOS .zip package (Apply Update -> Apply from ADB)
```
adb sideload lineage-packagename.zip
```

Reboot to System

### Manually updating from LineageOS Updater
Look at the [FAQS](https://github.com/xiaomi-spes-devs/OTA#faqs), question 4

### Reporting bugs / requesting features
Create an issue [here](https://github.com/xiaomi-spes-devs/OTA/issues) with the LineageOS exact version and steps on how to reproduce if it's an issue or what you want to be added into LineageOS.

Google Apps, Magisk, KSU and SafetyNet/Play Integrity related bugs/requests will be ignored and immediately closed !

Additionnally, if you aren't using exactly the same files available on the release section (ex: Using a different recovery like TWRP, a different kernel or being rooted), your issue will be ignored and immediately closed !

### FAQS
**Q1: How do I update my firmware after flashing LineageOS ?**

Answer: The latest firmware available for spes is included on the LineageOS .zip package, hence keeping your firmware updated on each updates.

**Q2: Are Google Apps included with LineageOS ?**

Answer: No. This is a vanilla build; install Google Apps separately by following the [LineageOS GApps guide](https://wiki.lineageos.org/gapps/), Use arm64 package.

**Q3: Is the LineageOS .zip package is signed and passes SafetyNet and Play Integrity ?**

Answer: Yes its signed and passes basic integrity on play store

**Q4: How do I update to another release of LineageOS ?**

**OTA update**

Go to Settings -> System -> System Update, check for updates, then download and install the available update.

**Local update**

Download the latest LineageOS .zip package from the release page to your phone. Go to Settings -> System -> System Update -> Click on the three dots -> Local update, then select the downloaded .zip package. The updater will install it automatically.

**Q5: I've followed the steps for updating LineageOS localy but the update disapeared from the list before I clicked on the reboot option from the Updater**

Answer: It's a known bug with LineageOS updater with local updates, simply follow again the steps to add the LineageOS .zip packages from your smartphone storage into the updater and the update will be available again from the Updater app.

**Q6: How long can I expect a new release of LineageOS ?**

Answer: Most likely the following month or a few weeks later if it's not an **HOTFIX** release, you won't have an exact date/time however since I do this out of my free time.

### Copyrights
Your warranty is now voided and I am not responsible for any bricks or bootloop.

Any apropriation/stealing and/or unauthorized redistribition of my work on the Internet without my constent is stricly forbidden.
