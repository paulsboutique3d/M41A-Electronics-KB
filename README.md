# M41A Pulse Rifle — Electronics Kit

**By [Paul's Boutique 3D](https://github.com/paulsboutique3d)**

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

## Hardware

| Component | Description |
|---|---|
| MCU | ATmega328P — Arduino Pro Mini 5V/16MHz |
| Audio | DFRobot DF1201S (DFPlayer) |
| Display | MAX7219 7-segment (2-digit) |
| LEDs | WS2811 × 2 per barrel |
| Bluetooth | KCX_BT_EMITTER V1.7 *(optional)* |
| Programmer | USBasp (ISP) |
| Battery | 2S LiPo (7.4V nominal) |

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

## Startup Sequence

1. Battery voltage on counter (e.g. `82` = 8.2V)
2. LED colour cycle
3. Counter sweep 00 → 99 → 00
4. Startup sound
5. Bluetooth status: `b0` (built-in speakers) or `b1` (Bluetooth active)
6. Green LED flash 3× — **ready**
7. Counter shows current ammo

> **No Bluetooth module?** The firmware auto-detects the KCX emitter at boot. If it's not installed, built-in speakers are used and Bluetooth controls are disabled. Install the module later — it will be detected on the next power-on.

## Build Info

The firmware is built with [PlatformIO](https://platformio.org/) targeting the ATmega328P via USBasp programmer.

| Setting | Value |
|---|---|
| Platform | Atmel AVR |
| Board | Pro Mini 5V/16MHz |
| Framework | Arduino |
| Fuses | L:0xFF H:0xDA E:0xFD |
| Watchdog | 2s (software-enabled) |

## License

This project is provided for personal prop-building use. Please contact [Paul's Boutique 3D](https://github.com/paulsboutique3d) for commercial licensing enquiries.
