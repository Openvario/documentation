# USB stick layout

FAT32 stick. Put this tree under `openvario/` for map updates, file transfer,
package updates (local `repo/`), and recovery images.

## Requirements

- Filesystem: **FAT32**
- Directory tree under `openvario/`

## Directory tree

```text
/
└── openvario/
    ├── maps/
    ├── repo/
    ├── download/
    │   └── xcsoar/
    ├── upload/
    │   └── xcsoar/
    └── images/
```

| Directory | Purpose |
|-----------|---------|
| `maps/` | Map files (`*.xcm` or compiled `.ipk`) for **Update Maps** |
| `repo/` | Local opkg mirror for incremental **Update System** |
| `download/` | Files copied from the device (for example IGC under `xcsoar/`) |
| `upload/` | Files copied to the device (`xcsoar/` → XCSoar home) |
| `images/` | Full SD images for recovery / **Flash SD Card** |

## Preparing the stick

- **Firmware images:** place files from
  [GitHub Releases](https://github.com/Openvario/OpenVario/releases) in
  `openvario/images/`.
- **Recovery boot file (Cubieboard classic recovery):** place
  `ov-recovery.itb` in `openvario/` (the directory itself). An older copy is
  available at [ftp.openvario.org/recovery/](https://ftp.openvario.org/recovery/).
- **Package repository:** the FTP `opkg/` tree is empty. Flash a full image
  from GitHub, or supply a local `repo/` mirror.

## Related

- [Update and recovery](update-and-recovery.md)
- [File transfer](../user-guide/file-transfer.md)
