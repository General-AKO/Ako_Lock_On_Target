# Positioning & Transform

When the configuration supports World UI, the Data Asset exposes several controls for placement and transformation.

## UI Location

**UI Location** is an offset relative to the target position; it is not an absolute world-space coordinate.

Conceptually:

```text
Final UI position = target position + configured offset
```

## UI Pivot

**UI Pivot** controls the point around which the widget is positioned and transformed.

Default:

```text
X = 0.5
Y = 0.5
```

This represents the center of the widget.

## UI Rotation

Controls rotation for supported world-space widget configurations.

## UI Scale

Controls world-space scale for supported World UI configurations.

Default:

```text
X = 1
Y = 1
Z = 1
```

## UI Draw Size

Defines the widget draw dimensions. The default is approximately `500 × 500`.

This is separate from the editor preview's logical design size.

## UI Geometry Mode

Controls the geometry representation used by a supported world-space widget. The default is **Plane**.

## Face Camera

Enable **Face Camera** when a world-space widget should automatically rotate toward the player's camera.

This is useful for target information panels and other world-space UI that should remain readable from different camera angles.
