# ADB

Here’s an extensive list of commands and utilities specific to Android terminals, particularly when using `adb` (Android Debug Bridge) and the Android shell (`adb shell`).


# Android Terminal Commands

## ADB (Android Debug Bridge) Commands

- **Check ADB version:**
  ```bash
  adb --version
  ```

- **Start ADB server:**
  ```bash
  adb start-server
  ```

- **Stop ADB server:**
  ```bash
  adb kill-server
  ```

- **List connected devices:**
  ```bash
  adb devices
  ```

- **Access Android device shell:**
  ```bash
  adb shell
  ```

- **Install an APK:**
  ```bash
  adb install path/to/app.apk
  ```

- **Uninstall an APK:**
  ```bash
  adb uninstall package.name
  ```

- **Pull a file from the device:**
  ```bash
  adb pull /path/on/device /path/on/host
  ```

- **Push a file to the device:**
  ```bash
  adb push /path/on/host /path/on/device
  ```

- **Reboot the device:**
  ```bash
  adb reboot
  ```

- **Reboot into bootloader:**
  ```bash
  adb reboot bootloader
  ```

- **Reboot into recovery mode:**
  ```bash
  adb reboot recovery
  ```

- **View device logs (logcat):**
  ```bash
  adb logcat
  ```

- **Take a screenshot:**
  ```bash
  adb exec-out screencap -p > screenshot.png
  ```

- **Record the screen:**
  ```bash
  adb exec-out screenrecord /sdcard/demo.mp4
  ```

- **Run a shell command on the device:**
  ```bash
  adb shell command
  ```

- **Forward a port from the device to the host:**
  ```bash
  adb forward tcp:port1 tcp:port2
  ```

- **Remove port forwarding:**
  ```bash
  adb forward --remove tcp:port
  ```

- **Get device properties:**
  ```bash
  adb shell getprop
  ```

- **Set a device property:**
  ```bash
  adb shell setprop key value
  ```

- **List installed packages:**
  ```bash
  adb shell pm list packages
  ```

- **Show detailed information about a package:**
  ```bash
  adb shell pm dump package.name
  ```

- **Grant a permission to an app:**
  ```bash
  adb shell pm grant package.name permission
  ```

- **Revoke a permission from an app:**
  ```bash
  adb shell pm revoke package.name permission
  ```

- **Force stop an application:**
  ```bash
  adb shell am force-stop package.name
  ```

- **Start an application:**
  ```bash
  adb shell am start -n package.name/activity.name
  ```

- **Broadcast an intent:**
  ```bash
  adb shell am broadcast -a action.name
  ```

- **Dump system status:**
  ```bash
  adb shell dumpsys
  ```

- **Check battery status:**
  ```bash
  adb shell dumpsys battery
  ```

- **Check memory usage:**
  ```bash
  adb shell dumpsys meminfo
  ```

- **List all processes:**
  ```bash
  adb shell ps
  ```

- **Kill a process by PID:**
  ```bash
  adb shell kill pidnumber
  ```

- **Run a shell command with root privileges (if device is rooted):**
  ```bash
  adb shell su -c command
  ```

- **Synchronize file system from the device to the host:**
  ```bash
  adb sync
  ```

- **Check the device’s connectivity status:**
  ```bash
  adb shell netstat
  ```

- **Manage packages using ADB (list, install, uninstall):**
  ```bash
  adb shell pm list packages
  adb shell pm install path/to/app.apk
  adb shell pm uninstall package.name
  ```

- **Check the device’s uptime:**
  ```bash
  adb shell uptime
  ```

- **Retrieve system information:**
  ```bash
  adb shell cat /proc/cpuinfo
  adb shell cat /proc/meminfo
  ```

- **Extract data from a specific path:**
  ```bash
  adb pull /sdcard/path/to/file /local/path
  ```

This list provides a comprehensive overview of commands for managing and interacting with Android devices using ADB and the Android shell.
