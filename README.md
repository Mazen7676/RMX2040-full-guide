# Realme 6i Guide

In this page, I'll cover everything you can do with Realme 6i (except unbricking a hard brick).

## Rollback to Android 10

**ALL YOUR DATA WILL BE DELETED**

### Pre-requirements

- Download the downgrade OTA file, you can find it in the files above, in oppostockrom website or type `#official_ozip` in [the official telegram group](https://t.me/narzo10club).

### Guide

1. There are 2 ways to install the OTA file:
    - Just open file manager and click it, it'll automatically rollback.
    - Reboot to recovery - install from storage and choose the OTA.

## Unlock Bootloader

**ALL YOUR DATA WILL BE DELETED**

### Pre-requirements

- Install the latest platform tools [here](https://developer.android.com/tools/releases/platform-tools).
- Install the latest drivers, you can find them in [Android USB Drivers](https://www.androidusbdrivers.com/oppo-realme-narzo-10-rmx2040-usb-drivers/) with guides on how to install them.
- Deep Testing for RMX2040 (you can find it in the files above, in the [the official telegram group](https://t.me/narzo10club) or on the Realme official site).

### Guide

1. Open Settings - About Phone - click Build Number multiple times until it prompts you for the lock screen password or shows the "You're now in developer mode" message.
2. Now search "USB debugging" and turn it on.
3. Install Deep testing for your phone
4. Click on "Start Applying" (if you don't see a warning screen or application submitted, click Query Verification Status then start the in-depth test), accept the warning screen, and submit the application.
5. Wait for about 1-2 hours; you should see "Review Successful."
6. Click "Start the in-depth test."
7. You should see a black screen with 3 or more command lines.
8. Connect the phone to the PC, open the platform tools file, click on the address bar where the file path is shown, and type `cmd`. This should open a command prompt window.
9. Now type this: `fastboot flashing unlock`.
10. This should open a warning on the phone, select using volume buttons "UNLOCK THE BOOTLOADER," then press the power button.
11. Then redo the first 2 lines (if you wish to continue with flashing recovery, rooting, and installing ROM).

## Debloat

Use Shizuku + Shizutools or Shizuku + Canta. you can find countless guides online.

## Unbrick Soft Brick

**ALL YOUR DATA WILL BE DELETED IF YOU CHOOSE USERDATA IN MCT OFP EXTRACTOR**

### Pre-requirements

- Download stock firmware; search "RMX2040 C.12 stock firmware" on your laptop if you're on Android 11 or "RMX2040 A.47 stock firmware" if you're on Android 10, you can find it in the files above or [here](https://oppostockrom.com/realme-6i-rmx2040).
- **(DO NOT USE ANDROID 11 FIRMWARE FOR ANDROID 10 OR ANDROID 10 FIRMWARE FOR ANDROID 11, IT WILL SOFT BRICK IT, if you accidentally do so, repeat the same guide with the correct firmware).**
- Unlocked bootloader.
- Download MCT OFP Extractor.

### Guide

1. Boot into bootloader; you can do this by holding power + volume down. 
2. If you're stuck in a bootloop or an infinite loading screen, hold power + vol up + vol down until it turns off, then release volume up. You should see 3 (or more) command lines on the left.
3. Unzip the stock firmware.
4. Open MCT OFP Extractor, choose the `.ofp` file from the unzipped folder and put it in a new folder (this should take some time).
5. Now copy all of the extracted files into the platform tools file after extracting them.
6. Connect the phone to the laptop.
7. Now open platform tools file nd click on the address bar where the file path is shown, type `cmd`, and press enter. This should open a command prompt.
8. Now type the following commands for each file that ends in `.img`:
   - `fastboot flash [img_name] [img_name.img]` (for example: `fastboot flash boot boot.img`)
9. If something refuses to flash, it's ok.
10. Now type: `fastboot reboot system` and everything should be back to normal.

## Unbrick Hard Brick

### Pre-requirements

- Install stock firmware; search "RMX2040 C.12 stock firmware" if you're on Android 11 or "RMX2040 A.47 stock firmware" if you're on Android 10, you can find it in the [Oppo Stock ROM](your-link-here) website.
- **(DO NOT USE ANDROID 11 FIRMWARE FOR ANDROID 10 OR ANDROID 10 FIRMWARE FOR ANDROID 11, IT WILL SOFT BRICK IT. If you accidentally do so, repeat the same guide with the correct firmware).**
- Install the latest drivers, you can find them in [Android USB Drivers](your-link-here) with guides on how to install them.
- Install MCT OFP Extractor.
- Install SP Flash Tool.

### Guide

- **IDK, ask in [t.me/narzo10group](https://t.me/narzo10club).**

## Install Custom Recovery (PBRP)

### Pre-requirements

- Rolled back to Android 10.
- Unlocked bootloader.
- USB debugging enabled.
- PBRP for RMX2020 (yes, this is not a typo).

### Guide

1. Download PBRP for RMX2020 (yes, this is not a typo) from [SourceForge](your-link-here).
2. Copy the entire zip file to your phone, unzip it on your computer, open the TWRP folder in the unzipped folder, copy `recovery.img`, and paste it in platform tools on your PC.
3. Remove the password from your mobile (do this whenever trying to open PBRP because decryption is broken).
4. Connect the phone to the PC, click on the address bar where the file path is shown, type `cmd`, and press enter. This should open a command line.
5. Enable file transfer on your phone, then type `adb reboot bootloader` in the cmd. If this doesn't work, try `adb reboot fastboot` (it should ask for a prompt on your phone to enable USB debugging, check always allow and allow, then type the command again).
6. You should see 3 lines on a black screen on your phone.
7. Type in the cmd window on your computer `fastboot flash recovery recovery.img` then `fastboot reboot recovery`.
8. Wait for a bit; you should see the PitchBlack recovery loading screen.
9. Click Install - choose the zip you previously copied to your phone - wait for a bit - press the home button - reboot - recovery to reboot back to the system.
10. Click reboot-system.

## Install Custom Recovery (TWRP)

### Pre-requirements

- Rolled back to Android 10.
- Unlocked bootloader.
- USB debugging enabled.
- TWRP for RMX2040 (you can find this in the [t.me/narzo10club](https://t.me/narzo10club) Telegram group).

### Guide

1. Download TWRP for RMX2040, unzip it on your computer, copy `recovery.img`, and paste it in platform tools on your PC.
2. Connect the phone to the PC, click on the address bar where the file path is shown, type `cmd`, and press enter. This should open a command line.
3. Enable file transfer on your phone, then type `adb reboot bootloader` in the cmd. If this doesn't work, try `adb reboot fastboot` (it should ask for a prompt on your phone to enable USB debugging, check always allow and allow, then type the command again).
4. You should see 3 lines on a black screen on your phone.
5. Type in the cmd window on your computer `fastboot flash recovery recovery.img` then `fastboot reboot recovery`.
6. Wait for a bit; you should see the TWRP loading screen.
7. To reboot back to the system, click reboot-system.

## Root:

**Warning:** **ALL YOUR DATA WILL BE DELETED**

### Pre-requirements:
1. Custom recovery installed
2. Magisk

### Guide:
1. Flash Magisk normally via PBRP. You can find countless guides online and also how to bypass SafetyNet check and hide root via Shamiko.

## Install ROM:

**Warning:** **ALL YOUR DATA (might) BE DELETED**

### Pre-requirements:
1. TWRP installed
2. GApps or FOSSApps of your preference (if not already included in the ROM)
3. A ROM of your choice on your PC (you can find RMX2020 ROMS that work for RMX2040 in [t.me/rmx2040roms](https://t.me/rmx2040roms)). I personally tried crDroid 12.1 ROM (NOT GSI) and it's working well so far. I will update on further testing.

### Guide:
1. Connect the phone to the PC.
2. Open Platform Tools, click on the address bar where the file path is shown, type `cmd`, and press Enter. This should open a command prompt.
3. Enable file transfer on your phone, transfer GApps (optional) and PBRP zip files from the PC to your phone.
4. Type `adb reboot recovery` in the cmd.
5. You should see TWRP loading screen (PBRP fastboot is broken).
6. Click Wipe - Advanced Wipe, select Data, Cache, Dalvik/ART Cache, and swipe to wipe.
7. Click the Home button - Reboot - Fastboot. You should be in TWRP fastbootd.
8. Type in the cmd window on your laptop: `fastboot erase metadata` and `fastboot erase system`.
9. Type `fastboot reboot recovery`.
10. Click Install, go to PBRP zip file location, click it, and swipe.
11. Click Home button - Reboot - Recovery.
12. You should be in PBRP now (TWRP doesn't allow ROMs other than RMX2040).
13. Click Advanced - ADB Sideload, check Wipe Dalvik Cache and Wipe Cache, and swipe.
14. Type in the cmd on your computer: `adb sideload [zip-file-name-of-installed-os.zip]` (don't include the square brackets).
15. If it says on the PC it failed at 48% or something similar, it's okay. Just check the phone to see if it says it's successful.
16. Click Cancel - Home - Wipe - Format Data - type "yes" - Enter.
17. Click Home - Reboot - System (Don't if installing GApps).

## Installing GApps or FOSSApps (optional):
1. In PBRP recovery, go to Install, navigate to the zip file location, click it, and swipe.
2. Go to Wipe - Format Data - type "yes" and enter.
3. Finally, go to Reboot - System.

## Install GSI (not recommended as it will most likely lag):

**Warning:** **ALL YOUR DATA WILL BE DELETED**

### Pre-requirements:
1. TWRP installed.
2. `vbmeta.img` file (extract it from stock firmware using MCT OFP Extractor or get it from [t.me/narzo10club](https://t.me/narzo10club) Telegram group).
3. GApps or FOSSApps of your preference if not already included in the GSI (optional).
4. A GSI of your choice on your computer. MUST be arm64 and NOT vndklite, and the code should start with "b" (bvN, bgN, bvS, bgS). I personally like dotOS from their official site or AOSP 14 if you prefer it.

### Guide:
1. Extract the zip or xz file using 7zip or WinRAR.
2. Connect your phone to the PC, open Platform Tools, and click on the address bar where the file path is shown. Type `cmd` and press Enter to open a CMD window.
3. Type `adb reboot fastboot`. You should see TWRP fastbootd.
4. Type the following:
   - `fastboot --disable-verification flash vbmeta vbmeta.img`
   - `fastboot reboot fastboot`
   - `fastboot erase system`
   - `fastboot flash system [name-of-gsi-img.img]` (don't include the square brackets)
   - `fastboot -w`
   - `fastboot reboot bootloader` (you should see a black screen with 3 or more lines)
   - `fastboot erase userdata`
   - `fastboot reboot system`

## Installing GApps or FOSSApps (optional):
1. Transfer the zip file from the PC to your phone.
2. Type `adb reboot recovery` in the CMD.
3. In TWRP recovery, go to Wipe and swipe.
4. Go to Install, navigate to the zip file location, click it, and swipe.
5. Go to Wipe - Format Data - type "yes" and enter.
6. Finally, go to Reboot - System.

---

If you encounter any issues, please let me know. If you find any mistakes, please tell me. I apologize for any grammar mistakes or misspellings as English isn't my mother language.
