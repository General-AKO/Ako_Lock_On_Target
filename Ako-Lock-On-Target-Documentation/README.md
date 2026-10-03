# ako Lock On Target

A flexible lock-on target and target UI system for Unreal Engine, designed for reusable target configuration, bone-based targeting, custom target indicators, and data-driven target information widgets.

## What this documentation covers

This documentation is written for users integrating **ako Lock On Target** into an Unreal Engine project. It explains the target-side setup, target-point configuration, reusable UI Data Assets, Status Widgets, world/screen UI settings, status elements, editor preview, common setups, and Blueprint integration responsibilities.

The system is designed so that the **target actor defines what can be targeted**, the **Target UI Data Asset defines how target information is presented**, and your **Blueprint/gameplay logic controls how targeting and gameplay values are driven**.

## Start here

New to the system? Follow this path:

1. [Introduction](getting-started/introduction.md)
2. [Installation & Project Setup](getting-started/installation.md)
3. [Your First Target](getting-started/first-target.md)
4. [Target Configuration](target-configuration/target-point-modes.md)
5. [Target UI Data Assets](ui/data-assets.md)
6. [Choose a UI Workflow](ui/custom-widget.md)

## System at a glance

```text
Target Actor
    │
    └── Lock-On Target Component
            │
            ├── Target Point / Bones
            ├── Lock-On Icon
            └── UI Target Settings
                    │
                    ▼
            Target UI Data Asset
                    │
                    ├── Custom Widget
                    └── Status Widget
                            │
                            └── Status Elements
```

## Documentation structure

- **Getting Started** — install the plugin and build your first configured target.
- **Core Concepts** — understand how the main pieces fit together.
- **Target Configuration** — configure skeletons, target points, bones, and icons.
- **Target UI** — create reusable UI Data Assets and configure screen/world presentation.
- **Status System** — build progress, segmented, and text-based target information.
- **Editor Preview** — use the built-in preview to refine target UI layouts.
- **Examples** — standard enemies, bosses, bone-based targeting, segmented health, and custom UI.
- **Troubleshooting** — common configuration issues and their fixes.
- **Reference** — compact reference tables for the main settings.

## Important integration note

The system is designed to work alongside your own Blueprint/gameplay logic. Target acquisition, input handling, camera behavior, health/stamina/shield values, and other project-specific gameplay rules are not tied to one mandatory gameplay architecture.
