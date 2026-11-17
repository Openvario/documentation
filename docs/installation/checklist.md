# Installation checklist

Complete before flight.

## Mechanical

- [ ] Cutout and screw pitch match the installed variant
      ([Panel cutout](panel-cutout.md))
- [ ] Machining clearance applied; unit seats without force
- [ ] Depth clear for case, connectors, and hoses
- [ ] Panel USB reachable; Stick Remote or rotary encoder secured if fitted

## Electrical

- [ ] Aircraft power polarity correct; feed protected ([Power](power.md))
- [ ] Peer devices on correct pinouts (IGC versus non-IGC)
- [ ] RJ45 loads within **500 mA** per port; total within **1.5 A** main fuse
- [ ] ACD, radio, and XPDR on independent circuit protection as required by
      their documentation

## Pneumatics (sensorboard)

- [ ] Static, TEK, and pitot on the correct barbs; leak-checked
      ([Pneumatics](pneumatics.md))

## Software

- [ ] Matching system image written ([Choose an image](choose-image.md))
- [ ] Touch calibration and display rotation complete
      ([First boot](first-boot.md))
- [ ] XCSoar Devices: OpenVario TCP **4352** on Device A with sensorboard;
      peers on Device B and above
      ([Sample installation](sample-installation.md))
- [ ] FLARM, variometer, and ACD show clean NMEA on the Devices monitor
- [ ] Audio variometer tones present if expected (`variod` enabled)
- [ ] Network available if maps or SSH are required
      ([Wi‑Fi](../user-guide/wifi.md))

## Ground verification

- [ ] Stable power cycles; no flicker or resets under load
- [ ] Display readability checked in the installed panel position

Fault finding: [Troubleshooting](../user-guide/troubleshooting.md).
