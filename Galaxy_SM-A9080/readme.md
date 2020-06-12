# Root Samsung Galaxy SM-A9080

This is a guide for rooting the galaxy A90 phone. 

## Unlock bootloader
1. First unlock developer mode by clicking build number by 7 times
1. Unlock OEM lock
1. Turn off the phone; unplug the phone; press volumn+ and volumn- combo and in the meanwhile plug the phone into PC
1. Long-press the Volume Up button to unlock the bootloader.

NOTE: **FAILED** to install and use *CROM SERVICE* due to its limited support for ANDROID 10 OS

## Download
- Firmware 链接:https://pan.baidu.com/s/17-CxZLb3UtPY9ld2QtdMZA  密码:xbb7 解压密码：sxrom.com
- adb/fastboot toolkit 
- Odin for windows and Jodin3 for macos (Catalina **DOES NOT** support this tool!)
- Magisk Manager

NOTE: make sure the firmware is newer than the original one by checking the build number. It should be larger than what is shown in system settings

## Root the phone
1. Download everything
1. Install Masgick Manager (If unavailable, set download to manual path: http://101.133.237.130/Magisk/Magisk_Latest.json)
1. Extract the firmware zip file and it will give you 5 tar files. Copy the tar file starting with the AP of your device.
1. Open the Magisk Manager and head over to Magisk Install>> Install>> Select and Patch a file-> locate the AP file.
1. the firmware will be patched and will be found in Internal Storage/emulated/0/Download/magisk_patched.tar. Transfer the patched file to your PC.
1. Turn OFF your Galaxy A90 5G and boot into DOWNLOAD MODE (by either use `adb reboot bootloader` or press volumn+- and plug the phone).
1. Now open the Odin tool. 
    1. For BL use the BL.tar.md5 file from stock firmware
    1. For AP use the patched.tar file
    1. For CP use the CP.tar.md5 file from stock firmware
    1. For CSC use the CSC.tar.md5 file from stock firmware
1. Press the Start button and wait for it to complete the flash.
1. Install the Magisk manager again.
1. Remove the USB cable and turn off the phone. Turn on the phone by holding volume up and power and release the button once you see the bootloader warning.
1. Finally, open Magisk Manager and click Install (set the path again as stated above).

NOTE: If the bootloader is older than current system version, a *write failed* problem might occur when using Odin. 

## Reference
A useful guide from https://www.getdroidtips.com/unlock-bootloader-root-galaxy-a90-5g/#Download_USB_Drivers
Download firmware for 20CNY from https://www.sxrom.com/rom/download/SM-A9080-CHC-A9080ZCU1ASJ1-A9080CHC1ASJ1.html

