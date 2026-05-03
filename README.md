# glove80-config

My personal ZMK configuration for the MoErgo Glove80. Built on top of [TailorKey](https://sites.google.com/view/tailorkey) by @moosy, tuned for macOS and daily use as a DevOps engineer.

## Layout

Base layer is [TailorKey](https://sites.google.com/view/tailorkey) with home row mods (HRM) on ASDF / JKL;. Modifiers are CTRL / ALT / CMD / SHIFT left to right on both hands.

### Layers

| # | Name | Access |
|---|------|--------|
| 0 | HRM macOS | default |
| 1 | Cursor | hold left outer thumb (tap = Backspace) |
| 2 | Symbol | hold Space (tap = Space) |
| 3 | Lower | hold inner left thumb (tap = tap dance → toggle) |
| 4 | Mouse | hold right outer thumb (tap = Enter) |
| 5–7 | Mouse slow / fast / warp | hold-tap inside Mouse layer |
| 8 | Magic | hold far-left key (RGB, Bluetooth, bootloader) |
| 9 | Dvorak | switch via Lower + 2 |

### HRM tuning

All 8 fingers use `balanced` flavor with per-finger tapping terms:

| Finger | Tapping term |
|--------|-------------|
| Index | 250ms |
| Middle | 260ms |
| Ring | 270ms |
| Pinky | 300ms |

`quick-tap-ms = 175ms`, `require-prior-idle-ms = 150ms` on all fingers.

### Top row

Media keys on the base layer — brightness, previous, next, play/pause, mute, volume. F1–F10 are on the Lower layer. I can't remember the last time I used an F key voluntarily.

### Key remaps

- **PgUp** → `Cmd+Shift+4` (area screenshot)
- **PgDn** → `Cmd+\`` ` (cycle windows of current app)

### Dvorak

Full hardware Dvorak layer with the same HRM modifiers on the same physical fingers — only the tap characters change. Switch layouts without touching OS settings.

- **Lower + 1** → QWERTY
- **Lower + 2** → Dvorak

### Cursor layer highlights

Hold the left outer thumb key to activate. Useful bits:

| Key | Action |
|-----|--------|
| G | Cmd+C |
| B | Cmd+V |
| T | Cmd+X |
| Z | Cmd+A |
| J K L ; | ← ↑ ↓ → |
| X / C | Select line / word |

### Combos

| Keys | Action |
|------|--------|
| Both T1 thumbs | Caps Lock |
| RH T4 + T1 | Sticky Hyper (Cmd+Ctrl+Alt+Shift) |
| RH T5 + T4 | Sticky Meh (Ctrl+Alt+Shift) |
| RH outer col R1+R2 | F11 / F12 |

## Flashing

Releases are built automatically on every push to main via GitHub Actions. Grab `glove80.uf2` from the [latest release](../../releases/latest) and drag it onto the Glove80 USB drive while in bootloader mode.

## Resources

- [TailorKey](https://sites.google.com/view/tailorkey) — the base layout this config builds on
- [ZMK docs](https://zmk.dev/docs)
- [Glove80 ZMK fork](https://github.com/moergo-sc/zmk)
- [Glove80 support](https://moergo.com/glove80-support)
