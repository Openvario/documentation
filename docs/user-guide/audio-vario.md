# Audio vario

With a [sensorboard](hardware-options.md), two daemons provide NMEA data to the
flight application:

| Daemon | Role |
|--------|------|
| **sensord** | Pressure sensors → NMEA |
| **variod** | Audio vario / speed-to-fly tones |

Enable or disable under [System Services](system-services-and-tools.md).
XCSoar/OpenSoar control volume and MacCready from the user interface.

Without a sensorboard, use an external XCSoar-compatible variometer
([Hardware options](hardware-options.md)).

## Sound hardware

| Output | Notes |
|--------|--------|
| **Onboard amplifier and speaker** | Default (connectorboard cinch) |
| **USB sound card** | Supported on many Cubieboard images; select the device in ALSA / XCSoar audio |

## Configuration files

| File | Daemon |
|------|--------|
| `/opt/conf/sensord.conf` | sensord |
| `/opt/conf/variod.conf` | variod |

Option reference: [Configuration](configuration.md).

Legacy wiki detail:
[sensord](https://www.openvario.org/doku.php?id=projects:series_00:software:sensord),
[variod](https://www.openvario.org/doku.php?id=projects:series_00:software:variod),
[NMEA](https://www.openvario.org/doku.php?id=projects:series_00:software:nmea).
