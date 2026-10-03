# Target UI Preview

Target UI Data Assets include a dedicated **Target UI Preview** area in the editor so you can refine the visual configuration without repeatedly launching the game.

## Preview layout

The editor preview is split into two views:

```text
┌──────────────────────────────┬─────────────┐
│                              │             │
│        Main Preview          │   Mini      │
│                              │   Preview   │
│                              │             │
└──────────────────────────────┴─────────────┘
```

The **Main Preview** is the primary editing view. The **Mini Preview** provides an overview of the complete design area.

## Main Preview

The main view includes a background grid. The grid scales with the current zoom level.

## Mini Preview

The miniature view shows the overall design canvas at a smaller scale. It is an overview rather than the primary navigation control.

## Pan

Move around the Main Preview with:

**Right Mouse Button + Drag**

The movement is direct and is not constrained to the design canvas.

## Zoom

Place the mouse over the **Main Preview** and use the mouse wheel.

The preview supports an approximate zoom range of:

```text
0.25× → 4.0×
```

Zoom is intentionally limited to the Main Preview area so the normal Details panel scrolling behavior is preserved elsewhere.

## Preview Design Size

The preview uses its own logical **Preview Design Size**. The default is approximately:

```text
1920 × 1080
```

This represents the editor's logical design canvas and is intentionally separate from **UI Draw Size**.

If your preview Blueprint uses another design resolution, update **Preview Design Size** in that Blueprint's defaults so the editor navigator matches the intended design space.
