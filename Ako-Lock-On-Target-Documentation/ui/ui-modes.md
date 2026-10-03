# UI Modes & Widget Space

The Data Asset provides two broad UI modes:

- **Normal UI**
- **World UI**

## Normal UI

Use the normal configuration for the standard non-world presentation used by your target-information workflow.

## World UI

Use World UI when the widget needs explicit world/WidgetComponent-style placement controls.

For supported configurations, additional controls become available for location, rotation, scale, geometry, and camera-facing behavior.

## Widget Space

When **World UI** is selected and the widget is not a Status Widget, Widget Space can be:

- **Screen** — the widget is rendered in screen space while remaining associated with the target UI setup.
- **World** — the widget is rendered as a world-space widget.

### Status Widget exception

The built-in Status Widget is forced to **Screen** space by the plugin.

Use a Custom Widget when you need a custom world-space status presentation based on your own Widget Blueprint architecture.
