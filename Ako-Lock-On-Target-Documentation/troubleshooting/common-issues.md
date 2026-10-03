# Common Issues

## The bone list is empty

Check that **Target Skeleton** is assigned to the correct Skeleton asset.

The component derives the available bone list from the assigned Skeleton and rebuilds it when the Skeleton changes.

## Bone Icon settings are missing

Bone-specific icon settings are context-sensitive. Select **Switch Between Bones** first.

## A bone uses the default icon

Check:

1. **Use Bone Icon Target** is enabled.
2. The bone exists in **Lock On Target Bones**.
3. The entry's Bone Icon contains a texture.

An empty Bone Icon intentionally falls back to the default **Lock On Icon**.

## The Status Widget is not using World widget space

This is expected. The built-in Status Widget is forced to **Screen** widget space by the plugin.

Use Custom Widget when you need your own world-space implementation.

## Text Display changes back to a bar

The plugin prevents this incompatible combination:

```text
Status Display Mode = Progress Bar Style
Display Style       = Text
```

Use:

```text
Status Display Mode = Progress Bar & Status Style
Display Style       = Text
```

## The preview does not appear

The editor customization loads the preview Blueprint expected by the plugin. Verify that the plugin content contains the required `UI_TargetUIPreview` Blueprint at its expected location.

A missing preview asset affects the editor preview, not the underlying Data Asset structure.

## The preview looks incorrectly scaled

Check **Preview Design Size** in the preview Blueprint. For a 1920×1080 design, use:

```text
Preview Design Size = 1920 × 1080
```

This setting is separate from **UI Draw Size**.

## Preview changes are not visible immediately

The editor customization listens for Data Asset property changes and refreshes the preview widgets. A custom preview Blueprint must also respond to `OnPreviewDataAssetChanged` and refresh its own visual state when needed.
