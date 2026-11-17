# Variants

OpenVario display variants share the RJ45 connectorboard and sensorboard.
The adapter board, housing, and firmware image name change with the panel.

## Classic Cubieboard displays

| Property | 7″ Pixel Qi | 7″ Texim / CH070 | 5.7″ Texim | 4.3″ Ampire | 7″ Ampire |
|----------|-------------|------------------|------------|-------------|-----------|
| Panel | PQ070WS01/02 | CH070OLDL-002 | CH057DLCL-002 | AM-480272… | AM-1280800… |
| Variant name | openvario-7-PQ070 | openvario-7-CH070 | openvario-57lvds | openvario-43rgb | openvario-7-AM070 |
| Resolution | 1024×600 | 800×480 | 640×480 | 480×272 | 1280×800 |
| FTP CAD | [pq070/](https://ftp.openvario.org/variants/pq070/) | [ch070/](https://ftp.openvario.org/variants/ch070/) | [57lvds/](https://ftp.openvario.org/variants/57lvds/) | [43rgb/](https://ftp.openvario.org/variants/43rgb/) | — |

Website overview: [variants](https://www.openvario.org/) → project variants table (also in the website repo).

## Firmware image names (5.1.0)

Current images: [OpenVario 5.1.0 release](https://github.com/Openvario/OpenVario/releases/tag/5.1.0).

| Hardware | Display | Asset |
|----------|---------|-------|
| Cubieboard 2 | CH57 | `OV-5.1.0-CB2-CH57.img.gz` |
| Cubieboard 2 | CH70 | `OV-5.1.0-CB2-CH70.img.gz` |
| Cubieboard 2 | PQ70 | `OV-5.1.0-CB2-PQ70.img.gz` |
| Raspberry Pi CM4 | CH57 | `OV-5.1.0-CM4-CH57.wic.bz2` (+ `.bmap`) |
| Raspberry Pi CM4 | PQ70 | `OV-5.1.0-CM4-PQ70.wic.bz2` (+ `.bmap`) |

CM4 images include Wi-Fi, serial ports, and sound support in 5.1.0.

## Legacy FTP images

[ftp.openvario.org/images/](https://ftp.openvario.org/images/) still hosts **22304** (2022) `.rootfs.img.gz` files for several panels, including 43-rgb and 57-lvds. Use the GitHub images for new installs.
