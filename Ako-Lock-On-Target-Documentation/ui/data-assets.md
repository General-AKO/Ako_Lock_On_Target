# UI Data Assets

The **Target UI Data Asset** separates target presentation from the Actor Blueprint.

Instead of rebuilding the same health bar, icon placement, and visual configuration on every target, create the UI definition once and reuse it.

```text
DA_Target_Enemy
    ↓
Enemy_A
Enemy_B
Enemy_C
Enemy_D
```

## What the asset contains

The editor organizes the configuration into areas such as:

- **Widget**
- **UI Target Info**
- **Status Elements**
- **Target UI Preview**

The asset is a reusable definition of presentation. It is not the live gameplay state itself.

## Reuse strategy

Use one Data Asset whenever several targets should share the same presentation.

Create another Data Asset when a target class needs a meaningfully different layout, such as:

```text
DA_Target_Enemy
DA_Target_Elite
DA_Target_Boss
DA_Target_NPC
```

This avoids duplicating identical configuration throughout actor Blueprints.
