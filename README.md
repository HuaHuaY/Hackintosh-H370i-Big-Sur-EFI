# Hackintosh-H370i-Big-Sur-EFI

H370i + i5 8600 + RTX 2070S + OpenCore 0.6.5

Modified from [SuperNG6](https://github.com/SuperNG6)/**[MSI-B360-Catalina-EFI](https://github.com/SuperNG6/MSI-B360-Catalina-EFI)**[(commit 8eea1d7)](https://github.com/SuperNG6/MSI-B360-Catalina-EFI/commit/8eea1d72913fae12a1b656ea2bf869e7fc4bb92f).

## Devices

- Processor: i5 8600

- Motherboard: ROG STRIX H370-I GAMING (BIOS version: 2811)

- Graphics:

    Intel UHD Graphics 630 (be used when using MacOS)

    NVIDIA GeForce RTX 2070 SUPER (be disabled)

- Memory: KLEVV 2666 16G * 2

- WLAN: Intel Wireless-AC 9560 160MHz (provided by motherboard)

- Storage: 

    Western Digital SN500 1T * 1 (Only Install Windows)

    Hikvision c2000 1T * 1 (Only Install MacOS)

    Seagate ST4000VX007 * 1

    HGST 725050A7E630 * 1 (In a USB hard drive box)

- Power: Corsair SF600 Platinum

- System: 

    Windows 10 20H2

    MacOS 11.3 Beta 20E5172i

- Monitor: SONGREN 240E (4k60hz/2k144hz, choosing 4k 60hz), HDMI or DP

![](https://cdn.jsdelivr.net/gh/HuaHuaY/Hackintosh-H370i-Big-Sur-EFI/img/0.0.png)

![](https://cdn.jsdelivr.net/gh/HuaHuaY/Hackintosh-H370i-Big-Sur-EFI/img/0.1.png)

![](https://cdn.jsdelivr.net/gh/HuaHuaY/Hackintosh-H370i-Big-Sur-EFI/img/0.2.png)

## Status

### USB

Every port works well but some funtions of are limited.

I make USBPorts.kext to follow 15 USB ports limit.

- 2 x USB 3.1 ports (at back panel, Type-A, support USB 2.0, 3.0 and 3.1)
- 3 x USB 3.0 ports (at back panel, Type-A, only support USB 2.0).
- 1 x USB 3.0 port (at back panel, Type-C SW, support USB 2.0 and 3.0).
- 2 x  USB 3.0 ports (internal, Type-A, only support one and support both USB 2.0 and 3.0).

### Bluetooth

Work well.

Use [OpenIntelWireless](https://github.com/OpenIntelWireless)/**[IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)**.

![](https://cdn.jsdelivr.net/gh/HuaHuaY/Hackintosh-H370i-Big-Sur-EFI/img/1.png)

### WLAN

Work well.

Use [OpenIntelWireless](https://github.com/OpenIntelWireless)/**[itlwm](https://github.com/OpenIntelWireless/itlwm)**.

![](https://cdn.jsdelivr.net/gh/HuaHuaY/Hackintosh-H370i-Big-Sur-EFI/img/2.png)

### Audio

Work well.

I use some config in `config.plist`:

```
<key>PciRoot(0x0)/Pci(0x1f,0x3)</key>
<dict>
	<key>device-id</key>
	<data>cKEAAA==</data>
	<key>layout-id</key>
	<data>BwAAAA==</data>
</dict>
```

![](https://cdn.jsdelivr.net/gh/HuaHuaY/Hackintosh-H370i-Big-Sur-EFI/img/3.png)

### Sleep

Work well.

### Hardware Decoding

Work well. And I ban the RTX 2070S in the config.plist.

![](https://cdn.jsdelivr.net/gh/HuaHuaY/Hackintosh-H370i-Big-Sur-EFI/img/5.png)

### HDMI and DP

One problem. If using HDMI with `-v` boot-args, it will stuck.

### Facetime and iMessage

Work badly in my macOS.

I don't have an iphone and I can't use the two functions since I begin to use Hackintosh, and I don't know it caused by my apple account or the config that the two functions are disabled.

