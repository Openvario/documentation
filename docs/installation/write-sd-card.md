# Write the SD card

## Important notices

- Writing an image **erases the entire microSD card**.
- Select the image for the installed **board and display** first —
  [Choose an image](choose-image.md). A wrong variant leaves the screen blank
  or unusable.

## Cubieboard 2 (`.img.gz`)

Download the matching `OV-5.1.0-CB2-*.img.gz` from
[GitHub Releases](https://github.com/Openvario/OpenVario/releases/tag/5.1.0).

### Linux

Write the compressed image directly to the card:

```sh
zcat OV-5.1.0-CB2-CH70.img.gz | sudo dd of=/dev/sdX bs=4M status=progress conv=fsync
```

Replace `/dev/sdX` with the whole-disk device (not a partition such as
`/dev/sdX1`). Confirm the device name before writing.

### Windows

1. Download the matching `.img.gz` from the release page.
2. Decompress with [7-Zip](https://www.7-zip.org/) (right-click →
   **7-Zip → Extract here**) to obtain a single `.img` file. Do not write the
   `.gz` file to the card.
3. Insert the microSD card. Note the drive letter; the entire card will be
   erased.
4. Write the `.img` with one of:
   - [Win32 Disk Imager](https://sourceforge.net/projects/win32diskimager/):
     select the `.img`, select the SD device, **Write**.
   - [Rufus](https://rufus.ie/): select the SD device, choose **Disk or ISO
     image**, select the `.img`, start the write.
5. Wait until the tool reports success, then eject the card safely.

If Windows prompts to format the card after writing, select **Cancel**.

## Raspberry Pi CM4 (`.wic.bz2`)

CM4 images are `.wic.bz2` plus a matching `.bmap`. The `.bmap` lists blocks
that contain data; `bmaptool` writes only those blocks (faster than a full
sparse `dd`) and can verify the result. Plain `dd` / `bzcat` ignores the
`.bmap`.

### Linux

With `bmaptool`:

```sh
sudo bmaptool copy --bmap OV-5.1.0-CM4-PQ70.wic.bmap \
  OV-5.1.0-CM4-PQ70.wic.bz2 /dev/sdX
```

Without `bmaptool`:

```sh
bzcat OV-5.1.0-CM4-PQ70.wic.bz2 | sudo dd of=/dev/sdX bs=4M status=progress conv=fsync
```

### Windows

1. Download `OV-5.1.0-CM4-*.wic.bz2` and the matching `.bmap` (required only
   for bmap-aware tools).
2. Decompress the `.wic.bz2` with 7-Zip to a `.wic` file.
3. Write the `.wic` as for a Cubieboard `.img` (Win32 Disk Imager or Rufus) to
   the whole SD device. Eject safely when complete.
4. Decline any Windows format prompts.

## Insert and boot

Insert the microSD card, apply power, and continue with
[First boot](first-boot.md).
