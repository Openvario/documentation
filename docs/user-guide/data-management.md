# Data Management (XCSoar)

XCSoar **Data Management** is the preferred method on current images to import
maps and files, export flights, and create or restore a full data backup,
without the classic OVMenu file-copy entries.

## Open Data Management

1. In XCSoar, open the menu (**F1** / Menu).
2. Go to **Config** → **Config page 2/3**.
3. Select **Data Management**.

Also available from some remote-stick menu layouts.

## Menu entries

| Entry | Purpose |
|-------|---------|
| **Navigation & Flight Resources** | Site files: maps, waypoints, airspace, and related paths |
| **Download manager** | Download maps and other repository files when online |
| **Export flights** | Copy IGC / flight logs to chosen storage (for example USB) |
| **Import data** | Copy selected files from USB (or other storage) into XCSoar’s data tree |
| **Backup manager** | Create a full data backup archive, or restore one |
| **Advanced File Explorer** | Browse and manage files under the data path |

Data resides on the data partition under `/home/root/data/XCSoarData` (not the
legacy `~/.xcsoar` layout alone).

## Import data

1. Insert a FAT32 USB stick containing the required files (maps `*.xcm`,
   waypoints, airspace, profiles, and similar).
2. Open **Data Management** → **Import data**.
3. Select the USB (or other) storage location.
4. Select the files to import.
5. Confirm. Recognised types are placed in matching subdirectories (maps,
   waypoints, airspace, …); unrecognised files are placed in the data root.

Select newly imported maps or files in XCSoar site / map settings as required.

## Backup manager

### Create a backup

1. Insert USB storage.
2. Open **Data Management** → **Backup manager**.
3. **Choose location** → select the USB device.
4. **Create backup**.

XCSoar writes a timestamped archive such as
`xcsoar_backup_YYYYMMDD_HHMMSS.tar` of the primary data path. Active IGC/NMEA
log files in use are skipped. **Not available while flying.**

### Restore a backup

1. Open **Backup manager** and select the storage that holds the `.tar`
   backup.
2. Select the backup in the list.
3. Run **Restore**.

Files are extracted into the primary data path. **Not available while flying.**
Restore overwrites matching data — create a fresh backup first if retention of
current data is required.

## Relation to the USB stick layout

The classic `openvario/upload/…` and `openvario/download/…` tree (see
[File transfer](file-transfer.md) and
[USB stick](../installation/usb-stick.md)) remains available via OVMenu /
transfer scripts. On XCSoar 5.x images, prefer **Import data**,
**Export flights**, and **Backup manager** when present — they address mounted
storage directly and place files in the correct directories.
