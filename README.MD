# 🐾 Custom Marlin 2.0.6 for Ender 3 Pro  

This is a **hand-tuned firmware** for **Creality Ender 3 Pro (V4.2.2 board)**.  
Z-offset is pre-configured but **must be fine-tuned** for your setup. EEPROM stores settings (`M500` to save changes).

<img align="right" width=175 src="buildroot/share/pixmaps/logo/marlin-250.png" />

## 📌 Version Info
- **Base:** Marlin 2.0.6
- **Author:** umittadelen
- **Target:** Ender 3 Pro V4.2.2
- **Last Updated:** 10/18/2025

## 🎛️ Hardware Setup
- **Printer:** Creality Ender 3 Pro
- **Mainboard:** V4.2.2 (STM32F103RET6, 512K)
- **Display:** CR10_STOCKDISPLAY / RET6_12864_LCD
- **Auto Bed Leveling:** BLTouch
- **Build Volume:** 220x220mm

---

<details>
<summary>

## ⚙️ Core Features
</summary>

### 🛡️ Safety & Reliability
- **NO_MOTION_BEFORE_HOMING**
- **Z_SAFE_HOMING** with 4mm clearance
- **EEPROM_SETTINGS** (M500/M501)
- **NOZZLE_PARK_FEATURE**

### 🎯 Auto Bed Leveling
- **BLTOUCH** support
- **AUTO_BED_LEVELING_BILINEAR** (5x5 grid)
- **USE_PROBE_FOR_Z_HOMING**
- **RESTORE_LEVELING_AFTER_G28**
- **ENABLE_LEVELING_FADE_HEIGHT**
- **Z_PROBE_OFFSET_RANGE ±20mm**

### 🎨 Enhanced Graphics & UI
- **DOGM_SD_PERCENT**, **PRINT_PROGRESS_SHOW_DECIMALS**
- **SHOW_REMAINING_TIME**, **ROTATE_PROGRESS_DISPLAY**
- **STATUS_HEAT_PERCENT**, **STATUS_FAN_FRAMES**
- **XYZ_HOLLOW_FRAME**
- **SHOW_BOOTSCREEN**, **SHOW_CUSTOM_BOOTSCREEN**
- **CUSTOM_STATUS_SCREEN_IMAGE**
</details>

---

## 🛠️ Building & Flashing
Use [PlatformIO in VSCode](http://docs.platformio.org/en/latest/ide/vscode.html).  
**Environment:** `STM32F103RET6_Creality`

### Flashing Steps
1. Build firmware in PlatformIO
2. Copy `.bin` file to SD card
3. Insert SD card into printer & power cycle
4. Wait for automatic update

### Post-Flash Configuration
1. `G28` – Auto-home
2. `G29` – Level bed
3. `M500` – Save settings
4. Fine-tune Z-offset: `M851 Z-X.X` (start ~ -2.5)
5. Test print and adjust

## 📌 Notes
- This firmware is tailored for **my setup** [*Stock Ender3 pro V4.2.2*].
- If you use it and something goes *kaboom* 💥… well, that’s on you.
> Precompiled versions can be found in 

## 📜 License
Based on [Marlin 2.0.6](https://github.com/MarlinFirmware/Marlin), published under [GPL](LICENSE).  
Keep it open, keep it free ♥

---
*Happy printing!*  
