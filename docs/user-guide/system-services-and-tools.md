# System Services and System Tools

Access via **Menu → Config → Configuration** → **System Services** or
**System Tools**.

## System Services

Start, stop, or restart installed units. Start also **enables** the unit across
reboots; stop **disables** it.

| Label | Unit | Purpose |
|-------|------|---------|
| **SSH server** | `dropbear.socket` | Remote shell |
| **Sensors** | `sensord.socket` / `sensord.service` | Pressure / air data |
| **Audio vario** | `variod.socket` / `variod.service` | Audio vario / STF tones |

### SSH

Dropbear is **disabled by default**.

1. Obtain an IP address ([Wi‑Fi](wifi.md), Ethernet, or USB tethering).
2. **System Services** → **SSH server** → start/enable.
3. From a PC: `ssh root@<openvario-ip>` (address shown on the Network page or
   System information).

Stop SSH when finished. Older images may still
expose OVMenu **Settings → SSH**.

### Sensors and audio vario

With a [sensorboard](hardware-options.md), keep both services running in
flight. Enable `variod` here if audio tones are absent. See
[Audio vario](audio-vario.md).

## System Tools

Scripts under `/usr/libexec/xcsoar/system-tools/`.

| Mode | Behaviour |
|------|-----------|
| **job** | Runs while XCSoar remains active |
| **exclusive** | XCSoar exits, the tool runs, then XCSoar restarts |

| Tool | Notes |
|------|--------|
| **Touchscreen calibration** | Exclusive. Touch each target; then set rotation again ([First boot](../installation/first-boot.md)). |
| **Sensor calibration** | Still air; no flow into pressure ports. |
| **Sensor initialization** | Clears sensorboard identity and calibration. Calibrate afterward. |
| **System information** | Versions, addresses, service status. |

Portrait calibration fails on some panels (issue #451); use landscape first.
Fallback: OVMenu **System → Calibrate Touch** (`ov-calibrate-ts.sh`).

## Custom tools

Place pairs in `/home/root/data/XCSoarData/tools/`: executable `<id>` and
`<id>.tool`. Listed as **User** (versus packaged **System**).

```text
name=Toggle XCSoar CPU log
description=Start or stop background XCSoar CPU measurement
instructions=Start logging before a replay or flight. Select again to stop.
mode=job
input=none
confirmation=required
```

| Field | Meaning |
|-------|---------|
| `name` | List label |
| `description` | Short summary |
| `instructions` | Help text before run |
| `mode` | `job` or `exclusive` |
| `confirmation` | for example `required` |
