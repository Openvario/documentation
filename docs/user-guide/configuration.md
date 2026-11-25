# Configuration files

## variod (`/opt/conf/variod.conf`)

| Option | Unit | Meaning | Example |
|--------|------|---------|---------|
| `deadband_low` | m/s | Lower deadband limit | `deadband_low -0.2` |
| `deadband_high` | m/s | Upper deadband limit | `deadband_high 0.5` |
| `pulse_length` | samples | Base pulse length | `pulse_length 12289` |
| `pulse_length_gain` | — | Pulse-length gain as climb increases | `pulse_length_gain 1.1` |
| `base_freq_pos` | Hz | Tone frequency for climb | `base_freq_pos 402` |
| `base_freq_neg` | Hz | Tone frequency for sink | `base_freq_neg 404` |

## sensord (`/opt/conf/sensord.conf`)

### Sensor corrections

Each pressure channel accepts offset and linearity:

```text
static_sensor  [offset] [linearity]   # Pa
tek_sensor     [offset] [linearity]   # Pa
dynamic_sensor [offset] [linearity]   # Pa
```

Examples:

```text
static_sensor  0.0 1.0
tek_sensor     0.0 1.0
dynamic_sensor 0.0 1.0
```

### NMEA output switches

| Option | Effect |
|--------|--------|
| `output_POV_E` | Enable POV E (TEK vario value) |
| `output_POV_P_Q` | Enable POV P and Q (static and dynamic pressure) |

## Global configuration

The legacy LaTeX guide reserved a global configuration section and left it
empty. Set those options in the files above, or in OVMenu and the OpenSoar
system menus.
