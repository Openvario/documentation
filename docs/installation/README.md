# Installation guide

This guide covers panel installation, electrical and pneumatic connections,
peer-device wiring, firmware selection, and initial configuration.

## Important notices

- OpenVario with XCSoar/OpenSoar is a **VFR navigation aid** only. It is not a
  substitute for primary flight instruments, traffic awareness, or terrain
  warning.
- Incorrect power pinouts can damage OpenVario and connected equipment.
- Validate the installation on the ground before flight.

## Prerequisites

- OpenVario unit of known display and board variant
- Aircraft 12 V supply with protection sized for OpenVario and any loads it
  supplies ([Power](power.md))
- Panel cutout dimensions for the installed housing ([Panel cutout](panel-cutout.md))
- Pressure hose for sensorboard installations ([Pneumatics](pneumatics.md))
- Serial interconnect cables for peer devices (FLARM, vario, ACD, and similar)
- Panel-mounted USB extension (recommended)
- External speaker, 4–32 Ω, if not already fitted
- microSD card (≥8 GB) and a PC if the system image must be written or replaced

## Contents

1. [System planning](system-planning.md) — dimensions, current, location
2. [Panel cutout](panel-cutout.md) — templates, depth, tolerance
3. [Power and fuses](power.md) — aircraft supply, accessory +12 V, panel USB
4. [Pneumatics](pneumatics.md) — static, TEK, and pitot (sensorboard)
5. [Sample installation](sample-installation.md) — example system and XCSoar Devices
6. [Hardware connectors](../user-guide/hardware-connectors.md) — back-panel pinouts
7. [Hardware options](../user-guide/hardware-options.md) — sensorboard, inputs, peers
8. [Choose an image](choose-image.md)
9. [Write the SD card](write-sd-card.md)
10. [First boot](first-boot.md) — touch calibration and display rotation
11. [Installation checklist](checklist.md)
12. [USB stick layout](usb-stick.md)
13. [Update and recovery](update-and-recovery.md)
14. [Troubleshooting](../user-guide/troubleshooting.md)

## Installation sequence

1. Optional bench verification with a known 12 V supply: display, touch, and
   rotation ([First boot](first-boot.md)). If the image is missing or incorrect:
   [Choose an image](choose-image.md), then [Write the SD card](write-sd-card.md).
2. [System planning](system-planning.md)
3. [Panel cutout](panel-cutout.md) — print the 1:1 template for the installed
   size; allow machining clearance and depth for connectors and hoses
4. Electrical and pneumatic work: [Power](power.md),
   [Pneumatics](pneumatics.md) if applicable, peer serial connections
   ([Hardware connectors](../user-guide/hardware-connectors.md),
   [Sample installation](sample-installation.md))
5. XCSoar Devices configuration: OpenVario TCP port **4352** on Device A when a
   sensorboard is fitted; peer devices on Device B and above.
   Complete the [Installation checklist](checklist.md).
