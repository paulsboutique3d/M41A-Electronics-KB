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

## Battery type
- ** 501855 7.4V 1400mAh SM Plug lipo Battery - Available on Ali express, Ebay, Amazon
- ** approx size 56-62mm Length, 18mm width, 8-10mm high

- <img width="651" height="302" alt="image" src="https://github.com/user-attachments/assets/04fcd103-bbc3-495f-9f63-7cc61bb67326" />


## Documentation

| Document | Description |
|---|---|
| [USER-GUIDE.md](USER-GUIDE.md) | How to operate the prop — startup, firing, magazine, Bluetooth, troubleshooting |
| [WIRING.md](WIRING.md) | Wire loom routing, lengths, and connector pinouts |


## License

This project is provided for personal prop-building use. 
