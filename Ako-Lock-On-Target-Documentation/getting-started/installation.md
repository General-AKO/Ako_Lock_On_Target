# Installation & Project Setup

Install the plugin into your Unreal Engine project using the plugin package supplied with your project/version.

After enabling the plugin, restart the editor when Unreal Engine requests it. The exact plugin installation process can vary depending on whether you are using a project-local installation or another distribution method.

## Before configuring a target

Make sure you have:

- An Unreal Engine project with the plugin enabled.
- An Actor Blueprint that should be targetable.
- A valid Skeleton when you plan to use bone-based targeting.
- A Widget Blueprint or the plugin's Status Widget workflow for target information.

## Recommended first setup

Configure one target completely before creating shared variations:

```text
Target Actor
    ↓
Lock-On Target Component
    ↓
Target Point
    ↓
Lock-On Icon
    ↓
Target UI Data Asset
    ↓
Widget / Status Widget
    ↓
Test in game
```

The plugin does not require your project to use one specific health system, controller, camera system, or input architecture.
