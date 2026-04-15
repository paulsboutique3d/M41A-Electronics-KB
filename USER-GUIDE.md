# M41A Pulse Rifle — User Guide

## Getting Started

Insert a fully charged battery (minimum 6.9V) and power on. The rifle runs through a boot sequence:

1. Battery voltage shown on the counter (e.g. `82` = 8.2V)
2. LEDs cycle through colours
3. Counter sweeps 00 → 99 → 00
4. Startup sound plays
5. Counter shows Bluetooth status: `b0` (built-in speakers) or `b1` (Bluetooth active) for 1.5 seconds
6. LEDs flash green 3× — **prop is ready**
7. Counter shows current ammo (or `00` if no magazine)

> **No Bluetooth module?** If the KCX Bluetooth emitter is not installed, the rifle automatically uses built-in speakers and shows `b0`. You can install the emitter later — the firmware will detect it on the next boot.

## Ammo Counter

The 2-digit display shows your current ammo count. The Thompson starts with **95 rounds** and the Remington has **6 shells**.

Your ammo is saved when you remove the magazine and restored when you reinsert it.

## Thompson (Main Gun)

### Burst Fire
With the fire selector set to **burst**, each trigger pull fires a **1–4 round burst** with a random sound effect. Muzzle LEDs flash yellow for each shot.

### Full Auto
With the fire selector set to **auto**, hold the trigger for **continuous fire** at ~15 rounds per second. Release the trigger to stop.

### Ammo Empty
When the counter reaches `00`, firing stops. Remove and reinsert the magazine to reload to 95 rounds.

## Remington (Shotgun)

Each trigger pull fires a single shot with a 2-second pump-action delay between shots. The counter briefly shows remaining shells, then returns to the Thompson count.

When all 6 shells are spent, the next trigger pull reloads.

## Magazine

| Action | What Happens |
|---|---|
| **Insert** | Ammo restored from last session (or 95 if fresh). Full magazine plays a short countdown animation. |
| **Remove** | Ammo saved. All firing and audio stops. Counter shows `00`. |

## Bluetooth Speaker

The prop can transmit audio wirelessly to a Bluetooth speaker instead of using the built-in speakers.

**Your Bluetooth setting is remembered.** If the battery dies or you power off while Bluetooth is on, it will automatically restore that setting on the next boot.

### Enable Bluetooth
1. Remove the magazine
2. Hold the Thompson trigger for **5 seconds**
3. You'll hear a BT-on sound, the counter shows `b1`, and LEDs flash **blue 3×**
4. The rifle tries to connect:
   - **Blue flashing Thompson LEDs** (first 10 seconds) — reconnecting to your last speaker
   - **Cyan flashing Thompson LEDs** (10–30 seconds) — scanning for a new speaker (put speaker in pairing mode)
   - **Solid green flash** — connected successfully
   - **Solid red flash** — no speaker found (timed out after 30s)
5. Built-in speakers are muted — all audio goes to the Bluetooth speaker

### Disable Bluetooth
1. Remove the magazine
2. Hold the Thompson trigger for **5 seconds**
3. You'll hear a BT-off sound, the counter shows `b0`, and LEDs flash **blue 3×**
4. Built-in speakers are re-enabled

### Switching to a Different Speaker
1. Disable Bluetooth (5s hold)
2. Turn off the old speaker, turn on the new speaker in pairing mode
3. Enable Bluetooth (5s hold)
4. The blue phase (first 10s) won't find the old speaker, then cyan phase scans and connects to the new one

### Power Cycle Behaviour
- **Bluetooth was on** → boots with speakers muted, counter shows `b1`, KCX reconnects to the last speaker automatically
- **Bluetooth was off** → boots normally with built-in speakers, counter shows `b0`
- **Bluetooth module not installed** → forces built-in speakers regardless of previous setting, counter shows `b0`

## Low Battery Warning

If the battery drops below **6.9V**, the rifle will:

1. Stop all audio and effects
2. Flash `--` on the counter 5 times
3. Enter a safe shutdown state

Recharge or replace the battery to resume operation.

## Quick Reference

| Action | Magazine | How | What It Does |
|---|---|---|---|
| Burst fire | In | Pull trigger (burst mode) | 1–4 shot burst |
| Full auto | In | Hold trigger (auto mode) | Continuous fire |
| Single shotgun shot | — | Pull Remington trigger | Fires one shell |
| Reload magazine | — | Remove and reinsert magazine | Restores ammo |
| Toggle Bluetooth | Out | Hold trigger 5 seconds | Turns BT on/off |

## Troubleshooting

| Symptom | Cause | Fix |
|---|---|---|
| Counter shows `33` and nothing works | Audio module failed to start | Power cycle the rifle |
| Counter shows `--` flashing then goes blank | Battery too low | Recharge battery |
| Bluetooth won't connect to speaker | Speaker not in pairing mode, or out of range | Make sure speaker is on and in pairing mode. Wait for cyan phase (after 10s) which scans for new devices |
| Bluetooth connects to wrong speaker | Old speaker still on | Turn off old speaker, disable BT, then re-enable. Cyan phase will find new speaker |
| No sound from built-in speakers | Bluetooth may still be on | Disable Bluetooth (hold trigger 5s, mag out) |
| Counter shows `b0` but BT module is installed | Module not detected at boot | Check KCX wiring to U7 connector, power cycle |
| Trigger doesn't fire | Magazine not fully seated | Remove and firmly reinsert magazine |
| Burst fires on magazine insert | Trigger noise during insertion | Normal — 2-second safety lockout prevents this |
| BT was on but no sound after reboot | Speaker powered off or out of range | Turn on speaker — KCX will auto-reconnect. Or toggle BT off/on to re-pair |
