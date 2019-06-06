# ioddfirmware
Upgrade a Zalman VE300 firmware to an iODD firmware.

Here is a working solution to get the latest IODD firmware on a Zalman VE-300.

- Download and extract the file zalman_ve300_to_iodd.7z
- Run the firmware writer iODD2531_user_fw_writer_02(R1288F)_x86.EXE as administrator
- Run the EDA tool as administrator
- Drag-and-drop the crosshair of the EDA tool on the disabled "Update" button of the firmware writer
- Activate the "enabled" checkbox in the EDA tool, right below the checked "visible" box. On eda  form, in the "Modify window" tab, untick the "WS_DISABLED" check box and click on "Set the window text" button : the "Update" button should now be enabled. 
- With your VE-300 device connected, press the "Update" button. The old updater is not so picky about the installed firmware on the device as the recent one.
- After finishing the update, power off the VE-300 and reconnect it. Now you have a "iodd2531" device with an outdated firmware.
- Run the latest firmware writer iODD_2531_user_fw_writer_04(R1600F)_x86.EXE. Since you have a valid iodd firmware on your device, the updater is happy with it. Just press the "Update" button.
- After finishing the update, power off the VE-300 and reconnect it. 
- Enjoy :-)

**Source** : Shoe user, in http://reboot.pro/topic/20174-how-to-flash-zm-ve400-with-original-firmware-from-iodd/
