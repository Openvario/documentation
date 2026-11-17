# Pneumatics (sensorboard)

This section applies only when a
[sensorboard](../user-guide/hardware-options.md) is fitted. Without a
sensorboard, TEK and pitot connections belong to the external variometer;
follow that equipment’s documentation (for example Larus or XCVario).

Sensorboard units provide three hose barbs on the case back
([Assembly](../assembly/README.md)):

| Port | Connection |
|------|------------|
| Static | Aircraft static |
| TEK / total energy | TEK probe or compensated static as installed on the glider |
| Dynamic / pitot | Pitot (indicated airspeed) |

Label hoses at both ends. Keep runs short. Avoid sharp bends and tees that
combine TEK with uncompensated static.

## Checks

1. Confirm leak-free joints at barbs and splices.
2. After initial flights, calibrate pressure sensors
   ([System Tools](../user-guide/system-services-and-tools.md)).
3. Wrong TEK or audio with working GPS/FLARM points to the plumbing
   or to Device A (OpenVario TCP **4352**) —
   [Troubleshooting](../user-guide/troubleshooting.md).

## Next

[Sample installation](sample-installation.md) · [Power](power.md).
