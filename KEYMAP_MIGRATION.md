# Corne to Totem Keymap Migration

## Overview
This document details the migration from Corne (42 keys) to Totem (38 keys) keyboard layout.

**Key difference**: Totem has 4 fewer keys - missing the leftmost and rightmost columns.

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
- Bluetooth controls maintained

---

### Raise Layer

**Left side - Removed column:**
- Row 1: (none, this was `TAB` position)
- Row 2: (none, this was `LCTRL` position)
- Row 3: (none, this was `LSHFT` position)

**Right side - Removed column:**
- Row 1: `ESCAPE` (top-right)
- Row 2: `GRAVE` (backtick, mid-right)
- Row 3: `TILDE` (bottom-right)

**Adaptation:**
- F6 removed (was between F5 and F7-F12 block)
- F12 removed (was at end of function key row)
- `PRCNT` (percent sign) removed from Corne's raise layer
- `ESCAPE`, `GRAVE`, and `TILDE` removed from raise layer
- All symbol keys (!, @, #, $, %, ^, &, *, etc.) maintained
- Bracket keys maintained: [], {}, ()
- Math operators maintained: -, =, _, +, \, |

---

## Summary

**Total removed keys**: 4 physical positions (2 columns)

**Critical missing functionality:**
1. `TAB` - Was on base layer left side, now removed
2. `BKSP` - Was on base layer right side, now removed
3. `ESC` - Was on raise layer right side, now removed
4. `DELETE` - Was on lower layer right side, now removed
5. `GRAVE/TILDE` - Were on raise layer right side, now removed
6. `SQT` (single quote) - Was on base layer right side, now removed

**Recommendations:**
- Consider adding `TAB` and `ESC` to a layer if needed frequently
- `BKSP` can be accessed via `BACKSPACE` on thumb keys in some layers
- Consider combo keys for frequently used missing keys
- The device layer with conditional activation (layers 1+2) provides additional functionality

**Successfully migrated:**
- All letter keys (Colemak DH layout)
- All number keys (0-9)
- Arrow keys and navigation
- Function keys (F1-F5, F7-F11)
- Most symbols and brackets
- Media controls (prev, next, vol up/down, play/pause)
- Bluetooth controls (BT0-4, BT_CLR)
- Modifiers adapted to available positions
