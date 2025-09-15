# 🐾 Custom Marlin 2.0.6 Firmware 🐾

<img align="right" width=175 src="buildroot/share/pixmaps/logo/marlin-250.png" />

Welcome to my custom fork of Marlin 2.0.6!  
This is a **hand-tuned** firmware for my **Creality Ender 3 Pro (V4.2.2 board)**.
It’s based on **Marlin 2.0.6** but sprinkled with some tweaks so my printer behaves nicely.
## 🍀 What I Changed
- [x] **NO_MOTION_BEFORE_HOMING**
- [x] **EEPROM_SETTINGS**
- [x] **NOZZLE_PARK_FEATURE**
- [x] Custom boot + status logos

## 🛠 Hardware Target
- **Mainboard:** Creality V4 (STM32F103RET6, 512K)
- **Display:** CR10_STOCKDISPLAY / RET6_12864_LCD

## 🔧 Building & Flashing
You can build this firmware using:
- [PlatformIO in VSCode](http://docs.platformio.org/en/latest/ide/vscode.html) (**recommended!**)

Environment: **`STM32F103RET6_Creality`**

Flashing steps (the simple way):
1. Build the firmware.
2. Put it on an SD card and feed it to the printer.
3. Restart and let the board do its magic ✨.

## 📌 Notes
- This firmware is tailored for **my setup** [*Stock Ender3 pro V4.2.2*].
- If you use it and something goes *kaboom* 💥… well, that’s on you.

## 📜 License
This project is based on [Marlin](https://github.com/MarlinFirmware/Marlin) 2.0.6
and published under the [GPL license](LICENSE).
Keep it open, keep it free ♥.