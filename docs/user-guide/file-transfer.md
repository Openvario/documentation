# File transfer

Two methods are available on current OpenVario images:

1. **XCSoar Data Management** — import, export, backup, and restore
   ([Data Management](data-management.md)). Preferred for XCSoar 7.45+ on 5.x
   images.
2. **USB stick with OVMenu / transfer scripts** — classic `openvario/…`
   directory tree. Required for OpenSoar workflows, recovery sticks, and older
   images.

## XCSoar Data Management

See [Data Management](data-management.md) for Import data, Export flights, and
Backup manager. Network downloads: [Wi‑Fi](wifi.md).

## Classic USB stick paths

Use a prepared [USB stick](../installation/usb-stick.md) (FAT32).

| Stick path | Direction | Typical use |
|------------|-----------|-------------|
| `openvario/upload/XCSoarData/` | Stick → device | Full XCSoar data tree upload |
| `openvario/upload/OpenSoarData/` | Stick → device | OpenSoar data tree upload |
| `openvario/upload/xcsoar/` | Stick → device | Legacy XCSoar home (fallback) |
| `openvario/download/XCSoarData/` | Device → stick | Download / sync of XCSoar data (including IGC) |
| `openvario/download/OpenSoarData/` | Device → stick | Same for OpenSoar |
| `openvario/igc/` | Device → stick | Legacy IGC-only download on older menus |
| `openvario/maps/` | Stick → device | Bulk maps via older **Update Maps** menu |

Transfer scripts use `/usb/usbstick` as the mount point and
`/home/root/data/XCSoarData` or `…/OpenSoarData` on the device.

## Practice notes

- Connect the stick before starting a transfer; avoid USB hubs when possible.
- Some sticks require reformatting to a single FAT32 partition.
- After importing maps, select them in XCSoar or OpenSoar map settings.

Map and task configuration for flight is covered in the XCSoar or OpenSoar
manual — [Further reading](further-reading.md).
