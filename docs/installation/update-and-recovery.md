# Update and recovery

## Prerequisites

- Prepared [USB stick](usb-stick.md)
- Reachable USB port on the OpenVario

## Update maps

Use when maps or Flarmnet data must be installed from the stick without network
access.

1. Connect the USB stick before power-on (or confirm it is mounted).
2. Apply power and press **Esc** for OVMenu.
3. Select **System** → **Update Maps**.
4. Wait until the update completes.

**Warning:** maps from the stick are installed even if they are older than maps
already on the device.

## Incremental system update (opkg)

If `openvario/repo/` on the stick contains a package repository:

1. Apply power and open OVMenu (**Esc**).
2. Connect the prepared USB stick.
3. Select **System** → **Update System**.
4. Review the listed packages, confirm, and wait for completion.

The historic FTP mirror at `ftp.openvario.org/opkg` is empty. For current
releases, prefer a full image from GitHub unless a local repository is hosted.

## Complete SD card flash (recovery)

Rewrite the entire SD card from the recovery environment. Allow about
15 minutes. Do not remove power until it finishes.

**Warning:** if recovery fails, remove the microSD card and rewrite it on a PC
([Write the SD card](write-sd-card.md)).

1. Place the required image in `openvario/images/` on the USB stick.
2. For classic Cubieboard recovery boot, also place `ov-recovery.itb` in
   `openvario/`.
3. Power off the OpenVario.
4. Connect the USB stick.
5. Apply power. The boot screen should display `!!! Recovery !!!`.
6. Wait for the recovery menu.
7. Select **Flash SD Card**.
8. Select the image version. If it is missing, check `openvario/images/`.
9. Select **Update All**, wait for completion, then reboot.

Use the same image files as a PC write, from
[GitHub Releases](https://github.com/Openvario/OpenVario/releases) for current
firmware. Use the FTP 22304 images only to stay on that release.

## Alternative: rewrite SD on a PC

Remove the microSD card and
[write a fresh image](write-sd-card.md) on a computer.
