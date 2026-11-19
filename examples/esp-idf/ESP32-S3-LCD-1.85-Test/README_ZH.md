# 板载外设检测和音频演示

[English](README.md) | [简体中文](README_ZH.md)

## 功能

演示板载外设检测、LVGL 音乐播放器和 ESP-SR 语音指令。状态页显示运动、RTC、电池、存储卡和 Wi-Fi 扫描等信息。

## 硬件需求

- ESP32-S3-LCD-1.85 开发板和 USB 数据线
- 播放音乐需连接扬声器，并使用根目录放有 MP3 文件的 FAT32 格式 microSD 卡
- 测量电池电压需连接兼容电池

## 怎么运行

使用 [仓库首页](../../../README_ZH.md) 所列版本的 ESP-IDF，在本目录打开 ESP-IDF 终端。

```bash
idf.py set-target esp32s3
idf.py build flash monitor
```

请烧录完整构建产物，让语音模型与应用程序一并写入各自的分区。

## 预期现象

LCD 显示状态页和音乐播放器。用 BOOT 和电源按键切换选择，同时按下两个按键确认。说 **Hi ESP** 后可发出英语语音指令。

## 常见问题

若播放器找不到曲目，请检查 microSD 卡是否为 FAT32 格式，以及 MP3 文件是否在卡的根目录。
