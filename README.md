In this thread, I'll cover everything you can do with Realme 6i (except unbricking a hard brick)

###Rollback to Android 10:

**ALL YOUR DATA WILL BE DELETED**

Pre requirements:
download the downgrade OTA file, you can find it [here](https://download.c.realme.com/flash/Rollbackpack/realme_narzo_10/new_ota_sign.zip) or type #official_ozip in t.me/narzo10club

Guide:
there are 2 ways to install the OTA file:
1: just open file manager and click it, it'll automatically rollback
2: reboot to recovery - install from storage and choose the OTA

##Unlock bootloader:

[!WARNING]**ALL YOUR DATA WILL BE DELETED**

**pre requirements:**
Install latest platform tools
Install latest drivers, you can find it in androidusbdrivers with guides on how to install

**Guide:**
open settings - about phone - click build number multiple times until it prompts you for the lock screen password or "you're now in developer mode" message is shown
now search "usb debugging" and turn it on

Install deep testing for RMX2040 (you can find it in {Mod edit: Reference to Telegram removed! Oswald Boelcke, Senior Moderator} telegram group or realme official site)
click on "start applying" (if you don't see a warning screen or application submitted, click Query verification status then start the in-depth test), accept the warning screen and submit application, wait for about 1-2 hours, you should see "Review successful" then click "start the in-depth test"
you should see a black screen with 3 or more command lines, connect the phone to the pc, open the platform tools file, click on the address bar where the file path is shown, type cmd, this should open a command prompt
now type this:
fastboot flashing unlock

this should open a warning on the phone, select using volume buttons "UNLOCK THE BOOTLOADER" then press the power button
then redo the first 2 lines (if you wish to continue with flashing recovery, rooting and installing ROM)

##Debloat:
use shizuku + shizutools or shizuku + Canta
you can find countless guides online

##Unbrick soft brick:

ALL YOUR DATA WILL BE DELETED IF YOU CHOOSE USERDATA IN MCT OFP EXTRACTOR

**Pre requirements:**
Install stock firmware, search "RMX2040 C.12 stock firmware" on your laptop, if you're on Android 11 or "RMX2040 A.47 stock firmware" if you're Android 10, you can find it [here](https://oppostockrom.com/realme-6i-rmx2040).
(DO NOT USE ANDROID 11 FIRMWARE FOR ANDROID 10 OR ANDROID 10 FIRMWARE FOR ANDROID 11, IT WILL SOFT BRICK IT, if you accidentally do so, repeat the same guide with the correct firmware)
Install [latest platform tools](https://developer.android.com/tools/releases/platform-tools)
Install latest drivers, you can find it [here](https://www.androidusbdrivers.com/oppo-realme-narzo-10-rmx2040-usb-drivers/) with guides on how to install
unlocked bootloader
download [mct ofp extractor](https://www.gsmware.com/2021/04/mct-ofp-extractor-tool.html)

**Guide:**
boot into bootloader, you can do this by holding power + volume down, if you're stuck in a bootloop or an infinite loading screen, hold power+vol up+vol down till it turns off, then release volume up, you should see 3 (or more) command lines on the left.
Unzip the stock firmware, Open mct ofp extractor, choose the .ofp file from the unzipped folder and put it in a new folder (should take some time)
now copy all of the extracted files into the platform tools file after extracting it
connect the phone to the laptop
now click on the address bar where the file path is shown, type cmd, press enter, this should open a command prompt
now type the following commands for each file that ends in .img:
fastboot flash [img_name] [img_name.img]
for example:
fastboot flash boot boot.img
it's quite a lot of files it's ok
if smth refuses to flash, it's ok
now type:
fastboot reboot system
and everything should be back to normal

##Unbrick hard brick:

**Pre requirements:**
Install stock firmware, search "RMX2040 C.12 stock firmware" if you're on Android 11 or "RMX2040 A.47 stock firmware" if you're Android 10, you can find it in oppostockrom website.
(DO NOT USE ANDROID 11 FIRMWARE FOR ANDROID 10 OR ANDROID 10 FIRMWARE FOR ANDROID 11, IT WILL SOFT BRICK IT, if you accidentally do so, repeat the same guide with the correct firmware)
Install latest drivers, you can find it in androidusbdrivers with guides on how to install
Install mct ofp extractor
Install sp flash tool

**Guide:**
idk ask in t.me/narzo10group

Install Custom Recovery (PBRP):
Pre requirements:
rolled back to android 10
unlocked bootloader
usb debugging enabled
PBRP for RMX2020 (yes this is not a typo)

Guide:
Download PBRP for RMX2020 (yes this is not a typo) from sourceforge, copy the entire zip file tp your phone, unzip it on your computer, open TWRP folder in the unzipped folder, copy recovery.img and paste it in platform tools on your PC
remove the password from your mobile (do this whenever trying to open PBRP because decryption is broken)
connect the phone to the pc, click on the address bar where the file path is shown, type cmd, press enter, this should open a command line
enable file transfer on your phone, then type "adb reboot bootloader" in the cmd, if this doesn't work try "adb reboot fastboot" (it should ask for a prompt in your phone to enable USB debugging, check always allow and allow then type the command again)
you should see 3 lines on a black screen on your phone
type in the cmd window on your computer "fastboot flash recovery recovery.img"
then "fastboot reboot recovery"
wait for a bit, you should see PitchBlack recovery loading screen
click install-choose the zip you previously copied to your phone-wait for a bit-press home button-reboot-recovery
to reboot back to system click reboot-system

Install Custom Recovery (TWRP):
Pre requirements:
rolled back to android 10
unlocked bootloader
usb debugging enabled
TWRP for RMX2040 (you can find this in {Mod edit: Reference to Telegram removed! Oswald Boelcke, Senior Moderator} telegram group)

Guide:
Download TWRP for RMX2040 (you can find this in {Mod edit: Reference to Telegram removed! Oswald Boelcke, Senior Moderator} telegram group), unzip it on your computer, copy recovery.img and paste it in platform tools on your PC
connect the phone to the pc, click on the address bar where the file path is shown, type cmd, press enter, this should open a command line
enable file transfer on your phone, then type "adb reboot bootloader" in the cmd, if this doesn't work try "adb reboot fastboot" (it should ask for a prompt in your phone to enable USB debugging, check always allow and allow then type the command again)
you should see 3 lines on a black screen on your phone
type in the cmd window on your computer "fastboot flash recovery recovery.img"
then "fastboot reboot recovery"
wait for a bit, you should see TWRP loading screen
to reboot back to system click reboot-system

Root:
Pre requirements:
custom recovery installed
Magisk
Guide:
flash magisk normally via PBRP, you can find countless guides online and also how to bypass safetynet check and hide root via shamiko

Install ROM:

ALL YOUR DATA (might) BE DELETED

pre requirements:
TWRP installed
GApps or FOSSApps of your preference if not already included in the GSI (optional)
A ROM of your choice on your PC (you can find RMX2020 ROMS that work for RMX2040 in {Mod edit: Reference to Telegram removed! Oswald Boelcke, Senior Moderator} telegram group)
(i personally tried crDroid 12.1 ROM NOT GSI and it's working well so far, will update on further testing)

Guide:
connect the phone to the pc, open platform tools, click on the address bar where the file path is shown, type cmd, press enter, this should open a command line
enable file transfer on your phone,transfer GApps (optional) and PBRP zip files from the PC to your phone then type "adb reboot recovery" in the cmd
you should see TWRP loading screen (PBRP fastboot is broken)
click wipe-advanced wipe
select data, cache, Dalvik/ART cache
swipe to wipe
click home button-reboot-fastboot
you should be in TWRP fastbootd
type in the cmd window in your laptop:
fastboot erase metadata
fastboot erase system
fastboot reboot recovery

then click install-go to PBRP zip file location-click it then swipe
then click home button-reboot-recovery

you should be in PBRP now (TWRP doesn't allow ROMs other than RMX2040)
click advanced-ADB sideload-check wipe dalvik cache and wipe cache then swipe
type in the cmd on your computer:
adb sideload [zip-file-name-of-installed-os.zip] (don't put the square brackets)
it should take some time
if it says on the PC it failed on 48% or smth it's ok, just check the phone if it says it's successful
then click cancel-home-wipe-format data-type yes-enter
then click home-reboot-system (don't if installing GApps)

Installing GApps or FOSSApps (optional):
in PBRP recovery, go to Install-go to zip file location-click it and swipe
then go to wipe-format data-type yes and enter
finally, go to reboot-system
enjoy!

Install GSI (not recommended as it will most likely lag):

ALL YOUR DATA WILL BE DELETED

Pre requirements:
TWRP installed
vbmeta.img file (extract it from stock firmware using mct ofp extractor or get it from {Mod edit: Reference to Telegram removed! Oswald Boelcke, Senior Moderator} telegram group)
GApps or FOSSApps of your preference if not already included in the GSI (optional)
A GSI of your choice on your computer MUST be arm64 and NOT vndklite and the code thing starts with b (bvN or bgN or bvS or bgS) (i personally like dotOS from their official site or AOSP 14 if you like it)
what does the code mean?
v means vanilla (no google apps)
g means GApps (with google apps)
N means no superuser (not pre-rooted - recommended)
S means superuser (pre-rooted - not recommended)

Guide:
extract the zip or xz file using 7zip or winrar
connect your phone to the PC, open platform tools and click on the address bar where the file path is shown, type cmd and press enter, this should open a CMD window
type "adb reboot fastboot"
you should see TWRP fastbootd
type the following:
fastboot --disable-verification flash vbmeta vbmeta.img
fastboot reboot fastboot
fastboot erase system
fastboot flash system [name-of-gsi-img.img] (don't put the quare brackets)
fastboot -w
fastboot reboot bootloader
(you should see black screen with 3 or more lines)
fastboot erase userdata
fastboot reboot system

Installing GApps or FOSSApps (optional):
transfer the zip file from the PC to your phone
type this: "adb reboot recovery"
in TWRP recovery, go to wipe and swipe
then go to Install-go to zip file location-click it and swipe
then go to wipe-format data-type yes and enter
finally, go to reboot-system

if you encounter any issues please tell me
if you find any mistakes please tell me
I apologize for any grammer mistakes or misspells as English isn't my mother language
