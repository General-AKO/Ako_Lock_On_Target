# Display Styles

Each Status Element has a **Display Style** that determines the primary visual form of the value.

| Display Style | Purpose |
|---|---|
| **Simple Progress Bar** | Standard continuous progress visualization |
| **Custom Progress Bar** | Segmented visual representation |
| **Text** | Text-based representation instead of a progress bar |

## Simple Progress Bar

Use for continuous resources such as health, stamina, shield, or another normalized value.

## Custom Progress Bar

Divides the visual representation into a configurable number of segments. This is useful for stylized indicators such as blocks, diamonds, stars, or custom shapes.

## Text

Displays the status as text rather than using a progress bar.

The editor prevents an incompatible combination between **Progress Bar Style** and **Text**. When that combination occurs, the display style is corrected to **Simple Progress Bar**.

For a text-focused status element, use:

```text
Status Display Mode = Progress Bar & Status Style
Display Style       = Text
```
