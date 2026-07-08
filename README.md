# ESP32-C3 GPS Firmware

ESP32-C3 WROOM-02 firmware for web flashing.

## Web flash (recommended)

Use the merged factory image — flash from address `0x0`:

- **File:** `merged-firmware.bin`
- **Flash link:** https://adam-weber.github.io/esp-webflash-toolkit/examples/hosted/?name=GPS-ESP32C3&bin=https://github.com/shenbinbin12/123/raw/main/merged-firmware.bin&chip=esp32-c3

Browser: Chrome or Edge. Connect USB, click Connect, then Flash.

## Files

| File | Purpose |
|------|---------|
| `merged-firmware.bin` | Factory image (bootloader + partitions + boot_app0 + app) — **use for online flash** |
| `firmware.bin` | App only (`0x10000`) — not for standalone web flash |
| `bootloader.bin` | Bootloader segment |
| `partitions.bin` | Partition table |
| `boot_app0.bin` | OTA data initial |

## Build info

- Board: ESP32-C3-DevKitM-1
- Flash: 4MB, QIO 80MHz
- Merged with esptool from PlatformIO build output
