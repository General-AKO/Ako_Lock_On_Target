# System Overview

The system is easiest to understand as a chain of reusable data and presentation layers.

```text
Target Actor
    │
    ├── Lock-On Target Component
    │      ├── Target Skeleton
    │      ├── Target Point
    │      ├── Target Bones
    │      ├── Lock-On Icon
    │      └── UI Target Settings
    │
    ▼
Target UI Data Asset
    │
    ├── Widget Type
    ├── UI Mode
    ├── Placement / Transform
    └── Status Elements
           │
           ├── Progress Bar
           ├── Segmented Bar
           └── Text
    │
    ▼
Widget Blueprint
    │
    ├── Custom Widget
    └── Status Widget
```

## Target Component

The target component stores configuration that belongs to the target actor, such as the Skeleton used for bone discovery, target-point behavior, target bones, icon settings, and references to target UI configurations.

## Target UI Data Asset

The Data Asset stores reusable instructions for how target information should be presented. It keeps visual configuration separate from individual actor Blueprints.

## Widget Blueprint

The final visual implementation is provided by either your own Custom Widget or a Status Widget class.

## Status Elements

A Status Widget can contain several status definitions so one target panel can show multiple gameplay values.
