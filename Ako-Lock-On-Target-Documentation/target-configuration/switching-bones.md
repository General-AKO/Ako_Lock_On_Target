# Switching Between Bones

Select **Switch Between Bones** when several Skeleton bones should be available as target points.

Configure the entries in **Lock On Target Bones**.

| Field | Purpose |
|---|---|
| **Bone Name** | Skeleton bone that can be used as a target point |
| **Bone Icon** | Optional icon used when the bone is active |

Example:

```text
Head       → HeadIcon
LeftArm    → ArmIcon
RightArm   → ArmIcon
Chest      → (empty)
```

If an entry has no Bone Icon, the default **Lock On Icon** is used as the fallback.

## Bone order

The component stores the configured bone entries in the order you provide them. Your Blueprint/lock-on logic can use the available entries according to the targeting behavior of your project.
