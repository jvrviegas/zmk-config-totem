# ZMK Config - Totem Keyboard

This repository contains my personal [ZMK firmware](https://zmk.dev/) configuration for the [GEIST Totem](https://github.com/GEIGEIGEIST/TOTEM) keyboard.

## Keymap

![Totem Keymap](totem%20keymap.png)

## Layout

The configuration uses a **Colemak-DH** inspired layout optimized for ergonomic typing with home row mods.

### Base Layer
- **Home Row Mods**: GUI/ALT/CTRL/SHIFT on the home row (A/R/S/T on left, N/E/I/O on right)
- **Alpha Layout**: Q-W-F-P-B / J-L-U-Y-; (top row)
- **Thumb Keys**: GUI, Lower layer, Space / Return, Raise/Backspace, Alt

### Lower Layer (Numbers & Navigation)
- **Numbers**: 1-0 across the top row
- **Media Controls**: Previous, Next, Volume Down, Volume Up, Play/Pause
- **Arrow Keys**: Left, Down, Up, Right on the right side

### Raise Layer (Symbols)
- **Special Characters**: !, @, #, $, % (left side)
- **Math/Programming**: ^, &, *, (, ) (right side)
- **Brackets/Braces**: -, =, [, ], \ / _, +, {, }, |
- **Capslock**: Available on left home row
- **Hyper Key**: Ctrl+Shift+Alt+GUI on thumb

### Device Layer (Bluetooth & Settings)
- **Conditional Layer**: Activated when both Lower and Raise are held
- **Bluetooth**: 5 BT profiles (BT0-BT4) and clear on right side
- **Brightness**: Decrease/Increase brightness controls
- **ESC**: Easy access escape key

## Features

### Custom Behaviors
- **Modified Hold-Tap**: Quick tap enabled (100ms) with tap-preferred flavor for responsive home row mods
- **Tapping Term**: 170ms for balanced typing experience

### Combos
- **Quote (')**: Combo on thumb keys (28+29)
- **Grave (`)**: Combo on middle fingers (8+9)
- **Tab**: Combo on left index fingers (0+1)
- **Delete**: Combo on right index fingers (7+8)

### Conditional Layers
- **Device Layer**: Automatically activates when both Lower and Raise layers are held simultaneously

## Building

This configuration uses GitHub Actions for automated firmware builds. Compiled firmware files are available in the [Actions tab](../../actions).

## Installation

1. Download the latest firmware from GitHub Actions
2. Flash the appropriate `.uf2` file for each half (left/right)
3. Connect via Bluetooth and start typing

## Customization

The main keymap is located at `config/totem.keymap`. Modify layers, combos, and behaviors to suit your preferences.

## Credits

- **Keyboard**: [GEIST Totem](https://github.com/GEIGEIGEIST/TOTEM)
- **Firmware**: [ZMK Firmware](https://zmk.dev/)
- **Keymap Visualization**: Created with [keymap-drawer](https://github.com/caksoylar/keymap-drawer)
