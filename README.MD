# 🐾Welcome to my custom fork of Marlin 2.0.6!  
This is a **hand-tuned** firmware for my **Creality E## ⚠️ Important Notes
- This firmware is **specifically tuned** for my Ender 3 Pro V4.2.2 with BLTouch
- Z-offset is pre-configured but **must be fine-tuned** for your setup
- Games are accessible during printing but don't interfere with print quality
- EEPROM stores your settings - use `M500` to save any changes

## 📌 Version Info
- **Base:** Marlin 2.0.6
- **Author:** umittadelen
- **Target:** Ender-3 Pro V4.2.2
- **Last Updated:** October 2025r 3 Pro (V4.2.2 board)** with **BLTouch auto bed leveling**.
It's based on **Marlin 2.0.6** but sprinkled with extensive tweaks and fancy graphics features.stom Marlin 2.0.6 Firmware 🐾

<img align="right" width=175 src="buildroot/share/pixmaps/logo/marlin-250.png" />

Welcome to my custom fork of Marlin 2.0.6!  
This is a **hand-tuned** firmware for my **Creality Ender 3 Pro (V4.2.2 board)**.
It’s based on **Marlin 2.0.6** but sprinkled with some tweaks so my printer behaves nicely.
## � Hardware Setup
- **Printer:** Creality Ender 3 Pro
- **Mainboard:** Creality V4.2.2 (STM32F103RET6, 512K)
- **Display:** CR10_STOCKDISPLAY / RET6_12864_LCD
- **Auto Bed Leveling:** BLTouch Probe
- **Build Volume:** 220x220mm bed

## ⚙️ Core Features
### 🛡️ Safety & Reliability
- [x] **NO_MOTION_BEFORE_HOMING** - Prevents movement before homing
- [x] **Z_SAFE_HOMING** - Safe Z-axis homing with BLTouch
- [x] **Z_HOMING_HEIGHT** - 4mm clearance during homing operations
- [x] **EEPROM_SETTINGS** - Persistent storage with M500/M501
- [x] **NOZZLE_PARK_FEATURE** - Smart nozzle parking

### 🎯 Auto Bed Leveling
- [x] **BLTOUCH** probe support
- [x] **AUTO_BED_LEVELING_BILINEAR** - 5x5 grid mesh
- [x] **USE_PROBE_FOR_Z_HOMING** - Probe-based Z homing
- [x] **RESTORE_LEVELING_AFTER_G28** - Maintains leveling after homing
- [x] **ENABLE_LEVELING_FADE_HEIGHT** - Gradual fade of corrections
- [x] **Z_PROBE_OFFSET_RANGE** - ±20mm adjustment range

## 🎨 Enhanced Graphics & UI
### � Display Enhancements
- [x] **DOGM_SD_PERCENT** - Shows print percentage (e.g., "73.5%")
- [x] **PRINT_PROGRESS_SHOW_DECIMALS** - Decimal precision progress
- [x] **SHOW_REMAINING_TIME** - Estimated time to completion
- [x] **ROTATE_PROGRESS_DISPLAY** - Cycles between Progress/Elapsed/Remaining
- [x] **STATUS_HEAT_PERCENT** - Visual heating progress bars
- [x] **STATUS_FAN_FRAMES** - 3-frame animated fan icons
- [x] **XYZ_HOLLOW_FRAME** - Optimized frame drawing

### 🎬 Boot & Status Screens
- [x] **SHOW_BOOTSCREEN** - Custom boot sequence
- [x] **SHOW_CUSTOM_BOOTSCREEN** - Custom boot logo
- [x] **CUSTOM_STATUS_SCREEN_IMAGE** - Custom status screen graphics

### 🎮 Built-in Entertainment
- [x] **MARLIN_BRICKOUT** - Classic brick-breaking game
- [x] **MARLIN_SNAKE** - Snake game for long prints
- [x] **MARLIN_INVADERS** - Space Invaders mini-game
- [x] **GAMES_EASTER_EGG** - Enhanced games menu styling

## 🔧 Probe Configuration
```cpp
NOZZLE_TO_PROBE_OFFSET { -45, -5, -2.5 }  // X, Y, Z offsets
Z_PROBE_OFFSET_RANGE_MIN -20              // Minimum Z offset
Z_PROBE_OFFSET_RANGE_MAX 20               // Maximum Z offset
GRID_MAX_POINTS_X 5                       // 5x5 leveling grid
GRID_MAX_POINTS_Y 5
```

## � Building & Flashing
You can build this firmware using:
- [PlatformIO in VSCode](http://docs.platformio.org/en/latest/ide/vscode.html) (**recommended!**)

**Environment:** `STM32F103RET6_Creality`

### Flashing Steps
1. Build the firmware in PlatformIO
2. Copy the `.bin` file to an SD card
3. Insert SD card into printer and power cycle
4. Wait for automatic firmware update ✨

### Post-Flash Configuration
1. **Auto-home:** `G28`
2. **Level bed:** `G29`
3. **Save settings:** `M500`
4. **Fine-tune Z-offset:** Use `M851 Z-X.X` (start with -2.5)
5. **Test print** and adjust as needed

## 🎯 Key G-codes
- `G28` - Auto home all axes
- `G29` - Run auto bed leveling
- `M851` - Set Z probe offset
- `M500` - Save settings to EEPROM
- `M501` - Load settings from EEPROM
- `M420 S1` - Enable bed leveling
- `M119` - Check endstop status

## 🎮 Games Menu
Access the built-in games through the LCD menu:
**Main Menu → Games**
- Play during long prints for entertainment
- Games include Brickout, Snake, and Space Invaders

## 📊 Display Features
- **Progress:** Shows percentage with decimals (47.3%)
- **Time Display:** Rotates between progress, elapsed, and remaining time
- **Heat Bars:** Visual progress bars for bed and hotend heating
- **Fan Animation:** 3-frame animated fan icon when running
- **SD Percentage:** Always visible print completion percentage

## 📌 Notes
- This firmware is tailored for **my setup** [*Stock Ender3 pro V4.2.2*].
- If you use it and something goes *kaboom* 💥… well, that’s on you.

## 📜 License
This project is based on [Marlin](https://github.com/MarlinFirmware/Marlin) 2.0.6
and published under the [GPL license](LICENSE).
Keep it open, keep it free ♥

---
*Happy printing! If something goes kaboom 💥... well, you've been warned! 😄*