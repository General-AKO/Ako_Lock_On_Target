# Introduction

**ako Lock On Target** is a configurable target-side system for Unreal Engine. It provides the data and editor workflow needed to describe how an actor behaves when exposed to a lock-on system and how target information should be presented.

Typical targets include:

- Enemies
- Bosses
- NPCs
- Interactive actors
- Other gameplay actors that need a lock-on target representation

## Main capabilities

- Multiple target-point modes.
- Specific-bone targeting.
- Switching between multiple target bones.
- Per-bone target icons with a default-icon fallback.
- Optional UI following of the active target point.
- Reusable **Target UI Data Assets**.
- Custom Widget Blueprint support.
- Built-in **Status Widget** workflow.
- Multiple configurable status elements.
- Simple, segmented, and text-based status displays.
- Normal and World UI configurations.
- World-space positioning controls for supported widget setups.
- Optional camera-facing behavior for world-space widgets.
- Editor preview with grid, pan, zoom, and miniature overview.

## The design principle

The plugin separates three concerns:

```text
Target configuration
        ↓
Reusable UI configuration
        ↓
Your gameplay / Blueprint logic
```

This separation lets you reuse a UI definition across many actors while keeping project-specific gameplay systems independent.
