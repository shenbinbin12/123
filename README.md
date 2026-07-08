# GPS ESP32-C3 固件在线烧录

## 在线烧录

1. 打开：**https://shenbinbin12.github.io/123/**
2. 使用 Chrome 或 Edge，USB 连接 ESP32-C3
3. 点击「安装 GPS 固件」，**首次务必勾选擦除 Flash**

## 文件说明（与 PlatformIO 一致）

| 文件 | Flash 地址 |
|------|------------|
| `bootloader.bin` | `0x0` |
| `partitions.bin` | `0x8000` |
| `firmware.bin` | `0x10000` |

## 串口监视器

波特率：**230400**
