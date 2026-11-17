# Wi‑Fi

Set up Wi‑Fi in XCSoar:
**Menu → Config → Configuration → Network.** Do not use OVMenu for Wi‑Fi on
current images.

## Hardware

| Platform | Radio |
|----------|--------|
| **Cubieboard 2** | No onboard Wi‑Fi — USB adapter (supported chipset and firmware) or phone tethering |
| **CM4** | Onboard Wi‑Fi; USB adapter also supported |

Hot-plug keeps a stable `wlan*` name (`openvario-wifi-link`).

### USB adapters (Cubieboard)

Select by chipset, not brand:

| Family | Driver / notes | Firmware on the image |
|--------|----------------|--------------------------|
| Realtek | `rtl8xxxu` (8188/8192/…) | `rtl8188`, `rtl8192`, `rtl8712`, `rtl8723`, `rtl8821` |
| Ralink | `rt2800usb` / RT53xx (**RT5370** historically reliable) | `linux-firmware-ralink` |
| MediaTek | `mt7601u`, `mt76x0u` | image firmware |
| USB Ethernet | RTL8150/8152, … | — |

If it does not associate, try another chipset from this table, or install
the missing firmware package.

## Connection procedure

1. Insert the USB adapter (Cubieboard) or enable the onboard radio (CM4).
2. Open the Network page → scan → select access point → enter passphrase.
3. Wait until connected status and an IP address appear.

Cubieboard images use ConnMan. CM4 images use NetworkManager.

- Use WPA. Open access points fail to associate on some builds.
- Enter the passphrase with the touchscreen or a keyboard, not the joystick alone.
- HTTPS requires a valid system clock (wait for sync or set time).
- CM4: the internal antenna adjacent to the LVDS bridge can cause display
  flicker — use `dtparam=ant2` with an external antenna (issue #417).

## USB tethering

RNDIS / CDC EEM are supported on Cubieboard and CM4 (issue #436):

1. Connect a data cable to the phone.
2. Enable USB tethering on the phone.
3. Confirm an IP address on the **Network** page.

Use with a [panel USB jack](../installation/power.md#panel-usb).

## OpenSoar / legacy

OpenSoar provides its own Wi‑Fi settings; data resides under `OpenSoarData`
([File transfer](file-transfer.md)). Legacy OVMenu/ConnMan shell notes remain
on the project wiki. Use **Network** on current images.
