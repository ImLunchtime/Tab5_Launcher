# Tab5-Launcher

## English
A "port" of the M5Launcher (sort of) for the Tab5, with LVGL GUI.

### What can it do?
You can select and load firmwares from the SD card (must be formatted in FAT32) and flash them into the device.

### Known issues:
 - Sometimes when flashing a firmware LVGL will run into errors rendering the progress bar so the UI freezes (The flashing process is still going though).
 - The file manager is not working due to path issues
 - The loaded firmware must not use the M5GFX/M5Unified library because if it uses M5GFX/M5Unified the device can't boot into the launcher again.

## 中文
将 M5Launcher "移植"到Tab5设备上，使用LVGL实现GUI。

### 它能做什么？
从SD卡中加载.bin格式的固件文件（SD卡必须使用FAT32文件系统）并将其烧录到设备，然后运行固件。

### 已知的问题
 - 有时烧录固件时，LVGL会出错导致进度条（界面）停止重绘，但是固件烧录进程依然会正常工作。
 - 文件管理器目前无法正常工作，因为默认路径不对。
 - 加载的固件必须不使用 M5GFX/M5Unified 库，否则会导致设备不再重启到Launcher。

## How to build
You can build using ESP-IDF, simply navigate to the project root and run `idf.py build`.
You should use the ESP-IDF shell in order to run idf.py commands.
Also, you can use your VS Code with the ESP-IDF Extension, simply open the project root directory in VS Code and the extension should automatically kick in.
## 如何编译
你可以使用ESP-IDF编译本项目。在项目根目录下执行`idf.py build`即可。
为了使用idf.py指令，你需要使用ESP-IDF的PowerShell或者CMD。
你也可以使用VS Code的ESP-IDF插件。用VS Code打开本项目根目录，插件会自动帮你配置，只需在VS Code中执行指令即可。
