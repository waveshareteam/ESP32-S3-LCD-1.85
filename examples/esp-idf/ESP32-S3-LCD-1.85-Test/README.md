# Board diagnostics and audio demo

[English](README.md) | [简体中文](README_ZH.md)

## What It Does

Runs board diagnostics alongside an LVGL music player and an ESP-SR voice command demo. The status screen includes motion, RTC, battery, storage and Wi-Fi scan information.

## Hardware Required

- ESP32-S3-LCD-1.85 development board and USB data cable
- Speaker and FAT32-formatted microSD card with MP3 files in its root directory for playback
- Compatible battery for the battery voltage check

## How to Run

Open an ESP-IDF terminal in this directory using the version listed in the [repository README](../../../README.md).

```bash
idf.py set-target esp32s3
idf.py build flash monitor
```

Flash the complete build so the speech model partition is written along with the application.

## Expected Result

The LCD shows the status screen and music player. Use BOOT and the power button to navigate, or press both together to confirm a selection. Say **Hi ESP** to activate English voice commands.

## Troubleshooting

If the music player cannot find any tracks, check that the microSD card uses FAT32 and the MP3 files are in its root directory.
