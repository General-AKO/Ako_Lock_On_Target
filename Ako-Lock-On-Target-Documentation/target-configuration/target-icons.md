# Target Icons

Target icons are configured at two levels: a global default icon and optional per-bone icons.

## Default Lock-On Icon

**Lock On Icon** is the standard target icon.

It also serves as the fallback when a selected target bone does not have its own icon.

This means you only need to assign unique icons where the visual design actually requires them.

## Bone Icons

Enable **Use Bone Icon Target** when the currently active bone should determine which icon is displayed.

This option is relevant to **Switch Between Bones** mode.

Example:

```text
Head      → Head marker
Chest     → Default marker
Left Arm  → Arm marker
Right Arm → Arm marker
```

## Icon size

**Custom Target Icon Size** controls the target icon dimensions. The component's default is approximately `50 × 50`.

Adjust it to match the scale and density of your HUD.
