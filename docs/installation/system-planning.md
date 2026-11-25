# System planning

Do this before cutting the panel.

## Dimensions

Measure the front of the unit to be installed. Display variants use different
cutouts and are not interchangeable.

| Class | Face (typical, mm) | Depth class (mm) |
|-------|--------------------|------------------|
| 5.7″ aluminium front | 133.4 × 104.8 | plate 10; case ≈62 (3D-print) or ≈80 (sheet-metal / SteFly) |
| 4.3″ | 126.5 × 72.5 | case ≈103 |
| Classic 7″ | 169 × 106.5 | **80.2** |

- Behind-panel clearance must cover the full **case** depth, not the front
  plate alone.
- Allow approximately 40 mm beyond the case for connectors and hose bends.
- Screw centres must match the cutout template. Do not enlarge the main cutout
  to correct screw-hole error.

Templates and figures: [Panel cutout](panel-cutout.md).

## Power consumption and supply

| Item | Value |
|------|--------|
| Aircraft bus | **12 V** nominal (≈**8–20 V** into the classic DC‑DC converter) |
| Computer alone | **&lt;500 mA** (≈6 W) |
| Each RJ45 accessory powered from OpenVario | up to **500 mA** (on-device fuse) |
| On-device main limit | **1.5 A** polyfuse |

Sum the computer draw and any load supplied through RJ45 +12 V. Equipment with
an independent aircraft supply (radio, transponder, many FLARM units, ACD)
retains its own circuit protection.

No cockpit circuit-breaker rating is published. Size the breaker for the
total load ([Power](power.md)).

## Location

- Display must remain readable in flight (glare and polarized sunglasses).
- Leave access to the microSD card, or remove the unit to write the image.
- Locate the [panel USB](power.md#panel-usb) jack within reach of the pilot.
- Keep sensorboard hose runs short and free of kinks
  ([Pneumatics](pneumatics.md)).

## Cooling

No cooling requirement is specified. Leave airflow behind the panel.

## Mounting

Secure the front frame to the panel with the screws specified by the cutout
template. Clearance guidance: [Tolerance](panel-cutout.md#tolerance).

## Next

[Panel cutout](panel-cutout.md) → [Power](power.md) → [Pneumatics](pneumatics.md).
