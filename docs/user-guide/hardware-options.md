# Hardware options

Hardware configurations and the corresponding software settings.
[Variants](../manufacturing/variants.md) · [Assembly](../assembly/) ·
[Sample installation](../installation/sample-installation.md).

## Sensorboard

| Configuration | Software |
|---------------|----------|
| **With sensorboard** | Run `sensord` / `variod` ([System Services](system-services-and-tools.md)). XCSoar **Device A** = OpenVario, TCP **4352** (MacCready / volume / TEK). External devices on Device B and above. |
| **Without sensorboard** | Do not configure Device A as OpenVario; disable unused `sensord`/`variod`. No onboard TEK or audio vario. FLARM and external variometers remain available on RJ45. |

## External XCSoar devices

Any driver shipped with XCSoar may be used if the peer speaks RS‑232 at
connectorboard signal levels.

1. Correct pinout ([Hardware connectors](hardware-connectors.md)); many IGC
   peers also accept **+12 V** on the same cable
   ([Power](../installation/power.md)).
2. **Config → Devices**: `ttyS*`, baud rate, driver.
3. Device A has priority. With sensorboard, assign OpenVario to Device A;
   otherwise assign the external variometer or GPS to Device A.

Examples: FLARM, LXNAV/LX, XCVario, Larus, Vega, BlueFly, Volkslogger, IMI,
AIR ACD, KRT2. Full list: [xcsoar.org/hardware](https://xcsoar.org/hardware/),
[manual](https://xcsoar.org/doc/).

### External variometer display

Instruments with their own screen (LXNAV S-class, XCVario/Larus, FLARM display)
use the same RJ45/serial connection and driver. **NMEA out** may feed a second
seat (master out → slave Devices in; confirm straight versus crossover cable).
OpenVario provides the navigation UI; the external unit provides the
instrument UI — or, without a sensorboard, the external unit is the
variometer.

## Platform and display

| Item | Notes |
|------|--------|
| **Cubieboard 2 / CM4** | Different images — [Choose an image](../installation/choose-image.md). Cubieboard: USB Wi‑Fi. CM4: onboard Wi‑Fi; prefer external antenna / `dtparam=ant2` (issue #417). |
| **Panel size** | Same connector concept; housing and image name change — [Variants](../manufacturing/variants.md). |

## Input

| Input | Notes |
|-------|--------|
| **Touchscreen** | Calibrate via [System Tools](system-services-and-tools.md) / [First boot](../installation/first-boot.md). Passphrase dialogs require touch or keyboard. |
| **Dual rotary** | Adapter extension; full UI without touch. |
| **Stick Remote** | USB HID grip (arrows/Enter, Menu/Esc/Fn, STF, optional PTT). Firmware: [Stick_Remote_Control_SteFly](https://github.com/OpenSoaring/Stick_Remote_Control_SteFly). FTP sketches: [Schematics](../manufacturing/schematics-and-pcb.md). Wiki `projects:remote_00`. XCI maps Menu/STF/PilotEvent. |

These inputs may be combined. Provide a
[panel USB jack](../installation/power.md#panel-usb).

## Connectivity and audio

Wi‑Fi / tethering: XCSoar **Network** — [Wi‑Fi](wifi.md).
Sound: [Audio vario](audio-vario.md).
