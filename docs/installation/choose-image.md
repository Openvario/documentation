# Choose an image

Select the system image that matches the **board** and **display**. A wrong
image leaves the screen blank or unusable.
[Variants](../manufacturing/variants.md).

## Current release

Download from the [OpenVario 5.1.0 GitHub release](https://github.com/Openvario/OpenVario/releases/tag/5.1.0).

| Board | Display | File |
|-------|---------|------|
| Cubieboard 2 | CH57 (5.7″) | `OV-5.1.0-CB2-CH57.img.gz` |
| Cubieboard 2 | CH70 (7″ Texim) | `OV-5.1.0-CB2-CH70.img.gz` |
| Cubieboard 2 | PQ70 (7″ Pixel Qi) | `OV-5.1.0-CB2-PQ70.img.gz` |
| Raspberry Pi CM4 | CH57 | `OV-5.1.0-CM4-CH57.wic.bz2` (+ `.bmap`) |
| Raspberry Pi CM4 | PQ70 | `OV-5.1.0-CM4-PQ70.wic.bz2` (+ `.bmap`) |

Release 5.1.0 provides Yocto Scarthgap whole-disk images, Linux 6.12,
XCSoar 7.45.1, and OpenSoar 7.43-3.23.8 with an application selector. Full
notes: [release_notes](../../release_notes/).

## Legacy FTP images

[ftp.openvario.org/images/](https://ftp.openvario.org/images/) hosts older
**22304** (2022) `.rootfs.img.gz` files. That set still covers panels absent
from the 5.1.0 GitHub release (notably **4.3″** / 43-rgb). The 5.7″ panel is
published on GitHub as **CH57**; use that image for new installs. Use FTP
images only to stay on the 22304 release.

## Next

[Write the SD card](write-sd-card.md).
