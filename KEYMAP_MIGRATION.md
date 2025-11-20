# Corne to Totem Keymap Migration

## Overview
This document details the migration from Corne (42 keys) to Totem (38 keys) keyboard layout.

**Key difference**: Totem has 4 fewer keys - missing the leftmost and rightmost columns.

---

## Current Keymap Configuration

### Base Layer (Default)
- **Layout**: Colemak DH
- **Homerow mods** implemented on row 2:
  - Left hand (ARST): GUI/A, ALT/R, CTRL/S, SHIFT/T
  - Right hand (MNEI): SHIFT/N, CTRL/E, ALT/I, GUI/O (inverted order)
- **Row 3 extra positions**: LCTRL (left), RIGHT_SHIFT (right)
- **Thumb cluster**: GUI, Lower (mo), SPACE | ENTER, Raise/BACKSPACE (lt), ALT

### Lower Layer
- **Row 1**: Numbers 1-9, 0
- **Row 2**: Media controls (prev, next, vol down, vol up, play/pause) | Arrow keys (left, down, up, right)
- **Row 3**: All transparent keys
- **Bluetooth controls**: Removed from this layer, available in device layer

### Raise Layer
- **Row 1**: Symbols (!, @, #, $, %) | Symbols (^, &, *, (, ))
- **Row 2**: CAPSLOCK, (empty) | Bracket symbols (-, =, [, ], \)
- **Row 3**: (empty) | Bracket symbols (_, +, {, }, |)
- **Thumb cluster**: Hyper key (CTRL+SHIFT+ALT+GUI) on left thumb
- **Note**: Function keys removed from raise layer

### Device Layer
- **Activation**: Conditional layer (activated when holding both lower and raise layers)
- **Row 1**: ESC, brightness controls | Bluetooth selection (BT0-BT4)
- **Row 2**: All empty
- **Row 3**: Bluetooth clear on bottom-right
- **Note**: Audio controls removed (available in lower layer)

### Combos
- **Single quote (')**: `,` + `.` (comma + period)
- **Grave (`)**: `Y` + `;` (Y + semicolon)
- **Tilde (~)**: SHIFT + grave combo
- **Double quote (")**: SHIFT + single quote combo
- **TAB**: `Q` + `W` (Q + W)
- **DELETE**: `U` + `Y` (U + Y)

---

## Missing Keys from Corne Layout

### Base Layer (Default)

**Left side - Removed column:**
- Row 1: `TAB` (top-left position)
- Row 2: `LCTRL` (mid-left position)
- Row 3: `LSHFT` (bottom-left position)

**Right side - Removed column:**
- Row 1: `BKSP` (top-right position)
- Row 2: `SQT` (single quote, mid-right position)
- Row 3: `RIGHT_SHIFT` (bottom-right position)

**Adaptation:**
- `LCTRL` moved to extra left position on row 3 (Totem's additional key)
- `RIGHT_SHIFT` moved to extra right position on row 3 (Totem's additional key)
- `TAB`, `BKSP`, and `SQT` removed from base layer
- **Homerow mods added**: Modifiers (GUI, ALT, CTRL, SHIFT) accessible via hold on ARST and MNEI keys

---

### Lower Layer

**Left side - Removed column:**
- Row 1: `TAB`
- Row 2: `LCTRL`
- Row 3: `LSHFT`

**Right side - Removed column:**
- Row 1: `DELETE` (was present in original Corne)
- Row 2: `trans` (transparent)
- Row 3: `trans` (transparent)

**Adaptation:**
- Control modifiers moved to row 3 extra positions
- Numbers and media controls remain fully accessible
- **Bluetooth controls moved** to device layer (conditional layer 3)

---

### Raise Layer

**Left side - Removed column:**
- Row 1: (none, this was `TAB` position)
- Row 2: (none, this was `LCTRL` position)
- Row 3: (none, this was `LSHFT` position)

**Right side - Removed column:**
- Row 1: `ESCAPE` (top-right) - **Now available in device layer top-left**
- Row 2: `GRAVE` (backtick, mid-right)
- Row 3: `TILDE` (bottom-right)

**Adaptation:**
- F6 removed (was between F5 and F7-F12 block)
- F12 removed (was at end of function key row)
- `PRCNT` (percent sign) removed from Corne's raise layer
- `ESCAPE` relocated to device layer top-left position
- `GRAVE` and `TILDE` removed
- All symbol keys (!, @, #, $, %, ^, &, *, etc.) maintained
- Bracket keys maintained: [], {}, ()
- Math operators maintained: -, =, _, +, \, |

---

## Summary

**Total removed keys**: 4 physical positions (2 columns)

**Keys still missing (not available anywhere):**
1. `F6` - Was in Corne raise layer (rarely used)
2. `F12` - Was in Corne raise layer (rarely used)

**Successfully adapted keys:**

*Via Layer-Tap and Layers:*
- ✓ **BACKSPACE** - Right thumb tap (with raise layer on hold via lt behavior)
- ✓ **ESC** - Device layer top-left (hold lower+raise simultaneously)
- ✓ **PERCENT (%)** - Raise layer B position (5th key top row)
- ✓ **All modifiers** - Homerow mods (ARST: GUI/ALT/CTRL/SHIFT, MNEI: inverted)
- ✓ **Hyper key** (CTRL+SHIFT+ALT+GUI) - Raise layer left thumb

*Via Combos:*
- ✓ **TAB** - `Q` + `W` combo
- ✓ **DELETE** - `U` + `Y` combo
- ✓ **Single quote (')** - `,` + `.` combo
- ✓ **Double quote (")** - SHIFT + single quote combo
- ✓ **Grave (`)** - `Y` + `;` combo
- ✓ **Tilde (~)** - SHIFT + grave combo

**Recommendations:**
- F6 and F12 can be added to empty layer positions if needed (rarely used)
- All commonly used keys are now accessible
- Device layer centralizes system controls (Bluetooth, brightness)

**Successfully migrated:**
- All letter keys (Colemak DH layout)
- All number keys (0-9)
- Arrow keys and navigation
- Function keys (F1-F5, F7-F11)
- Most symbols and brackets
- Media controls (prev, next, vol up/down, play/pause)
- Bluetooth controls (BT0-4, BT_CLR) - in device layer
- All modifiers via homerow mods (GUI, ALT, CTRL, SHIFT)
