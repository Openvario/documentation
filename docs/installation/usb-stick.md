# USB stick layout

A FAT32 USB stick with a fixed directory tree supports map updates, file
transfer, package updates (when a repository is present), and recovery images.

## Requirements

- Filesystem: **FAT32**
- Directory tree under `openvario/` as specified below

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
- **Package repository:** the FTP `opkg/` tree is empty. Prefer a full image
  flash from GitHub unless a local `repo/` mirror is maintained.

## Related

- [Update and recovery](update-and-recovery.md)
- [File transfer](../user-guide/file-transfer.md)
