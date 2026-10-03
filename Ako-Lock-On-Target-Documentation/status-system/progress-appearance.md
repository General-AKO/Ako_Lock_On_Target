# Progress Bar Appearance

Bar-based status styles expose appearance controls that let the same status system support both clean HUD bars and more stylized visual indicators.

## Fill Color and Opacity

Controls the color and opacity used by the progress visualization.

## Progress Bar Image

Defines the texture used for the visual shape of the bar.

## Progress Bar Size

Controls the dimensions of the visual element:

- `X` = Width
- `Y` = Height

## Segment Count

For **Custom Progress Bar**, Segment Count determines how many visual pieces represent the full value.

Example:

```text
10 segments
100% → 10 visible units
50%  → 5 visible units
20%  → 2 visible units
```

Segment Count changes the presentation only. It does not change the underlying gameplay value.

## Noise Opacity

Controls the visibility of the noise layer.

## Noise Strength

Controls the detail/strength of the noise effect. A value of `0` disables the effect.
