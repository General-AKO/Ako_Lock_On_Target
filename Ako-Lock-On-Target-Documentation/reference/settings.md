# Main Settings Reference

## Lock-On Target Component

| Setting | Description |
|---|---|
| **Target Skeleton** | Skeleton used to populate available target bones. |
| **Target Point** | Selects target-point behavior. |
| **Custom Z Height** | Vertical target-point position from `-1` to `+1`. |
| **Follow Target Point** | Determines whether target UI follows the active target point. |
| **Selected Bone** | Bone used by Specific Bone mode. |
| **Lock On Target Bones** | Bones available in Switch Between Bones mode. |
| **Use Bone Icon Target** | Uses per-bone icons when bone switching is active. |
| **Lock On Icon** | Default target icon and fallback icon. |
| **Custom Target Icon Size** | Size of the target icon. |
| **UI Target Settings** | References target UI Data Assets. |

## Target UI Data Asset — Widget

| Setting | Description |
|---|---|
| **Widget Type** | Custom Widget or Status Widget. |
| **Info Widget** | Widget class used by Custom Widget mode. |
| **Status Widget Class** | Widget class used by Status Widget mode. |
| **Status Widget Alignment** | Center / Top / Bottom / Left / Right alignment. |
| **Background Color** | Status panel background color. |
| **Border Color** | Status panel border color. |

## Target UI Data Asset — UI Target Info

| Setting | Description |
|---|---|
| **UI Mode** | Normal UI or World UI. |
| **Widget Space** | Screen or World for supported configurations. |
| **UI Pivot** | Widget transformation pivot. |
| **UI Location** | Offset relative to the target. |
| **UI Rotation** | Rotation for supported world-space widgets. |
| **UI Scale** | Scale for World UI. |
| **UI Draw Size** | Widget draw dimensions. |
| **UI Geometry Mode** | Geometry mode for supported world-space widgets. |
| **Face Camera** | Faces the player's camera in supported world-space configurations. |

## Status Element

| Setting | Description |
|---|---|
| **Status Display Mode** | Progress Bar Style or Progress Bar & Status Style. |
| **Display Style** | Simple Progress Bar, Custom Progress Bar, or Text. |
| **Segment Count** | Number of visual segments for Custom Progress Bar. |
| **Fill Color and Opacity** | Progress visual color and opacity. |
| **Progress Bar Image** | Texture used for the visual shape. |
| **Progress Bar Size** | Width and height of the progress visual. |
| **Noise Opacity** | Visibility of the noise layer. |
| **Noise Strength** | Detail/strength of the noise effect. |
| **Status Text** | Main status text configuration. |
| **Description Text** | Additional text settings in Text display mode. |
| **Auto Wrap Text** | Wraps description text when needed. |

## Default values noted by the editor implementation

| Setting | Approximate default |
|---|---:|
| Custom Target Icon Size | `50 × 50` |
| UI Pivot | `0.5, 0.5` |
| UI Scale | `1, 1, 1` |
| UI Draw Size | `500 × 500` |
| Segment Count | `8` |
| Preview Design Size | `1920 × 1080` |
| Preview Zoom | `0.25× → 4.0×` |
