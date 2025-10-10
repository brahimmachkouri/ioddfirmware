# Upgrade Zalman VE-300 firmware to an iodd 2531 firmware

![Zalman VE-300](https://raw.githubusercontent.com/brahimmachkouri/ioddfirmware/master/LD0003234649_2.jpg)

Here is a working solution to get the latest IODD firmware on a Zalman VE-300.

- Download and extract the file [zalman_ve300_to_iodd.7z](https://github.com/brahimmachkouri/ioddfirmware/raw/master/zalman_ve300_to_iodd.7z).
- Run the firmware updater iODD2531_user_fw_writer_02(R1288F)_x86.EXE as administrator. Warning: It's the firmware for FAT/exFAT. *Only this FAT release works with the EDA tool on Windows 11.* If you want to use NTFS, you first have to flash the old FAT firmware before you can flash the latest NTFS firmware with the regular IODD firmware flasher tool. On IODD's website, the letter "N" at the end (e.g., in R1288N) stands for NTFS support, while the letter "F" (e.g., in R1288F) stands for FAT/exFAT support.
- Run the EDA tool as administrator
- Drag-and-drop the crosshair (icon bottom right) of the EDA tool on the disabled "Update" button of the firmware writer
- Activate the "enabled" checkbox in the EDA tool. On eda  form, in the "Modify window" tab, uncheck the "WS_DISABLED" check box and click on "Set the window text" button : the "Update" button should now be enabled. 
- With your VE-300 device connected, press the "Update" button. The old updater is not so picky about the installed firmware on the device as the recent one.
- After finishing the update, power off the VE-300 and reconnect it. Now you have a "iodd2531" device with an outdated firmware.
- Run the latest firmware writer iODD_2531_user_fw_writer_04(R1600F)_x86.EXE. Since you have a valid iodd firmware on your device, the updater is happy with it. Just press the "Update" button. Maybe you'll find newer versions of the 2531 firmware in this page : http://iodd.kr/wordpress/support/download/#tab-e72d0adcf55af0bdf71
- After finishing the update, power off the VE-300 and reconnect it. 
- *Important*: You must use 2'048 bytes sector size on the NTFS partition to let the device discover the ISO files in the _ISO folder. If there is an unsupported sector size of, e.g., 4'096 bytes, the device will not find the disc images and only report "No Disc".
- Enjoy :-)

**Source** : D5AA96 user, in http://reboot.pro/topic/20174-how-to-flash-zm-ve400-with-original-firmware-from-iodd/
