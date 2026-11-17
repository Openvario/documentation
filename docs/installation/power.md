# Power and fuses

## Aircraft supply

Connect the OpenVario power port to the aircraft **12 V** bus (nominal).
Classic builds accept approximately **8–20 V** and regulate to **5 V** logic
([Assembly](../assembly/README.md) for DC‑DC adjustment on self-built units).

| Item | Value |
|------|--------|
| Computer alone | **&lt;500 mA @ 12 V** (≈6 W) |
| Inadequate supply | Resets or display blanking under load (CM4: issue #417) |

Connector identification: [Hardware connectors](../user-guide/hardware-connectors.md).
Reversed polarity can destroy the unit.

## Accessory +12 V on RJ45

On IGC-style RJ45 connectors, pins **1–2** may supply **+12 V** to a peer device
on a straight-through cable
([Hardware connectors](../user-guide/hardware-connectors.md)).

- Maximum **500 mA** per jack (on-device polyfuse)
- This current contributes to the aircraft feed and the **1.5 A** main fuse
  budget
- Not all peer devices accept +12 V on pins 1–2; consult the peer documentation
- For operation independent of OpenVario, supply the peer from the aircraft bus

## On-device fuses

| Location | Rating | Spare part (Farnell) |
|----------|--------|----------------------|
| Adapter main `F1` | **1.5 A** self-resetting | 1597003 |
| Each RJ45 | **500 mA** | 1597001 |

See [Bill of materials](../manufacturing/bill-of-materials.md).

## Cockpit circuit protection

No circuit-breaker rating is published. Protect the OpenVario feed and any
loads on its RJ45 +12 V. Size the breaker for that total
([System planning](system-planning.md)).

## Panel USB

Extend one USB port to a panel or console jack for storage devices, Wi‑Fi
adapters, phone tethering, keyboard, or
[Stick Remote](../user-guide/hardware-options.md). Use a dedicated extension
with strain relief; avoid hubs.
[USB stick layout](usb-stick.md).

Previous: [Panel cutout](panel-cutout.md). Next:
[Pneumatics](pneumatics.md) → [Sample installation](sample-installation.md).
