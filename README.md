# GPS ESP32-C3 Firmware

ESP32-C3 GPS 固件，支持浏览器在线烧录（与 PlatformIO 本地 3 文件烧录方式一致）。

## 在线烧录（推荐）

1. 打开 GitHub Pages：**https://shenbinbin12.github.io/123/**
2. 使用 Chrome 或 Edge，USB 连接开发板
3. 点击「安装 GPS 固件」，首次安装建议勾选擦除 Flash

若 Pages 未开启，请到仓库 Settings → Pages → Branch 选 `main` / `(root)`。

## 烧录文件（与 PlatformIO 相同）

| 文件 | Flash 地址 |
|------|------------|
| `bootloader.bin` | `0x0` |
| `partitions.bin` | `0x8000` |
| `firmware.bin` | `0x10000` |

## 本地烧录

使用 PlatformIO Upload，或手动用 esptool 按上表地址写入上述 3 个文件。

## 说明

- 不要使用 `merged-firmware.bin`（merge 会修改 bootloader 头，可能导致启动失败）
- 串口监视器波特率：230400
