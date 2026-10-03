# Target Point Modes

The target point determines where the targeting system considers the current target location to be.

## Default

Uses the target's standard target position.

Use this when you do not need a specific bone or custom vertical position.

## Use Specific Bone

Uses one selected Skeleton bone as the target point.

Useful for points such as:

- Head
- Chest
- Spine
- Hand
- Other body or weapon-related bones

The exact position follows the target's animation because the location is bone-based.

## Use Custom Z Height

Uses a normalized vertical control instead of a specific bone:

| Value | Meaning |
|---:|---|
| `-1` | Bottom of the target |
| `0` | Middle of the target |
| `+1` | Top of the target |

This is useful when you want a higher or lower lock-on point without depending on a dedicated Skeleton bone.

## Switch Between Bones

Allows several bones to act as available target points. Configure them in **Lock On Target Bones**.

This is useful when your lock-on gameplay logic needs to move the active target point between body locations while keeping the same actor as the target.
