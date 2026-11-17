# Data Management (XCSoar)

XCSoar **Data Management** imports maps and files, exports flights, and
backs up or restores the data tree. On current images it replaces the OVMenu
file-copy entries.

## Open Data Management

1. In XCSoar, open the menu (**F1** / Menu).
2. Go to **Config** → **Config page 2/3**.
3. Select **Data Management**.

Also on Stick Remote menus that list Data Management.

## Menu entries

| Entry | Purpose |
|-------|---------|
| **Navigation & Flight Resources** | Site files: maps, waypoints, airspace, and related paths |
| **Download manager** | Download maps and other repository files when online |
| **Export flights** | Copy IGC / flight logs to chosen storage (for example USB) |
| **Import data** | Copy selected files from USB (or other storage) into XCSoar’s data tree |
| **Backup manager** | Create a full data backup archive, or restore one |
| **Advanced File Explorer** | Browse files under the data path |

Data is on the data partition at `/home/root/data/XCSoarData`, not under
`~/.xcsoar`.

## Import data

1. Insert a FAT32 USB stick containing the required files (maps `*.xcm`,
   waypoints, airspace, profiles, and similar).
2. Open **Data Management** → **Import data**.
3. Select the USB (or other) storage location.
4. Select the files to import.
5. Confirm. Known types go into their directories (maps, waypoints, airspace).
   Other files go in the data root.

Select imported maps and files in the XCSoar site and map settings.

## Backup manager

### Create a backup

1. Insert USB storage.
2. Open **Data Management** → **Backup manager**.
3. **Choose location** → select the USB device.
4. **Create backup**.

XCSoar writes a timestamped archive,
`xcsoar_backup_YYYYMMDD_HHMMSS.tar`, of the XCSoar data directory. Open IGC
and NMEA logs are skipped. **Not available while flying.**

### Restore a backup

1. Open **Backup manager** and select the storage that holds the `.tar`
   backup.
2. Select the backup in the list.
3. Run **Restore**.

Files are extracted into the primary data path. **Not available while flying.**
Restore overwrites matching files. Take a backup first to keep the current data.

## Relation to the USB stick layout

The classic `openvario/upload/…` and `openvario/download/…` tree (see
[File transfer](file-transfer.md) and
[USB stick](../installation/usb-stick.md)) remains available via OVMenu /
transfer scripts. On XCSoar 5.x images, use **Import data**,
**Export flights**, and **Backup manager**. They copy to and from the mounted
stick and put files in the matching directories.
