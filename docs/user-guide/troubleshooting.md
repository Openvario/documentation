# Troubleshooting

## No boot / blank display

Incorrect image ([Choose an image](../installation/choose-image.md)), failed SD
write ([Write the SD card](../installation/write-sd-card.md)), or
[Update and recovery](../installation/update-and-recovery.md).

## Incorrect touch

Recalibrate and set rotation ([First boot](../installation/first-boot.md),
[System Tools](system-services-and-tools.md)). Portrait calibration fails on
some panels (issue #451) — use landscape. Check
[input configuration](hardware-options.md).

## SSH connection refused

Dropbear is disabled by default — enable in
[System Services](system-services-and-tools.md). An IP address is required
([Wi‑Fi](wifi.md)).

## No Wi‑Fi / association failure

Use XCSoar **Network** (not OVMenu). Cubieboard requires a supported USB
chipset ([Wi‑Fi](wifi.md)). HTTPS requires a valid clock. CM4 display flicker:
external antenna / `dtparam=ant2` (issue #417).

## USB tethering

Enable tethering on the phone, then confirm an IP address on **Network**.

## Missing or incorrect audio

Enable `variod` in System Services. Onboard versus USB sound:
[Audio vario](audio-vario.md). Without sensorboard, use an external variometer
([Hardware options](hardware-options.md)).

## Power instability / flicker / resets / accessory failure

Check supply and DC‑DC trim ([Power](../installation/power.md), issue #417).
**1.5 A** main or **500 mA** RJ45 fuse may have opened. Pinouts:
[Hardware connectors](hardware-connectors.md).

## Update failure

Verify stick layout and continuous power
([Update and recovery](../installation/update-and-recovery.md),
[USB stick](../installation/usb-stick.md)).

## No serial / FLARM / external variometer

Pinout, baud rate, driver, and `ttyS*` assignment —
[Hardware connectors](hardware-connectors.md),
[Hardware options](hardware-options.md), Devices monitor.

## No TEK / tones / MacCready–volume

Configure Device A as OpenVario TCP **4352** with services enabled, or use an
external variometer ([Hardware options](hardware-options.md)).

## Touch inactive / Stick Remote silent

Calibrate; verify rotary or Stick Remote wiring and panel USB
([Hardware options](hardware-options.md)).
