# M41A Pulse Rifle — Electronics Kit

**By [Paul's Boutique 3D](https://paulsboutique3d.com)**

A drop-in electronics package for the M41A Pulse Rifle prop, bringing the iconic weapon to life with sound, light, and an interactive ammo counter.

## What It Does

- **Ammo counter** — 2-digit 7-segment display tracks rounds for both the Thompson (95 rounds) and Remington (6 shells), with magazine memory via EEPROM
- **Muzzle flash LEDs** — WS2811 addressable LEDs on both barrels flash on every shot
- **Fire select** — potentiometer switches between burst fire (1–4 round random bursts) and full-auto (~15 rounds/sec)
- **Audio** — DFPlayer DF1201S module plays unique sounds for startup, burst fire (8 variants), full-auto, and shotgun shots
- **Magazine detection** — microswitch detects magazine insert/removal, saves and restores ammo count
- **Bluetooth audio** *(optional)* — KCX_BT_EMITTER module transmits all audio wirelessly to a Bluetooth speaker. Auto-detected at boot — install it any time or leave it out
- **Battery monitoring** — oversampled ADC with low-voltage cutoff (6.9V) and graceful shutdown
- **Watchdog protection** — 2-second hardware watchdog prevents firmware lockups


## Documentation

| Document | Description |
|---|---|
| [USER-GUIDE.md](USER-GUIDE.md) | How to operate the prop — startup, firing, magazine, Bluetooth, troubleshooting |
| [WIRING.md](WIRING.md) | Wire loom routing, lengths, and connector pinouts |

## Features at a Glance

| Gesture | Magazine | What It Does |
|---|---|---|
| Thompson pull | In | Burst fire (1–4 shots, random sound) |
| Thompson hold | In | Full-auto fire |
| Thompson hold 5s | Out | Toggle Bluetooth on/off |
| Remington pull | — | Single shotgun shot / reload at 0 |
| Insert magazine | — | Restore ammo, countdown animation |
| Remove magazine | — | Save ammo, stop all effects |



## License

This project is provided for personal prop-building use. 