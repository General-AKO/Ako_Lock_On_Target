# Target Skeleton

**Target Skeleton** identifies the Skeleton associated with the target.

When a Skeleton is assigned in the editor, the component reads its reference bones and refreshes the available bone list used by bone-based target settings.

## Why it matters

The Skeleton is used for:

- Specific-bone targeting.
- Bone switching.
- Per-bone target icons.

## Recommended workflow

Assign the correct Skeleton **before** configuring bone-based options.

If you replace the Skeleton later, the available bone list is rebuilt from the new Skeleton.

## Empty bone list

If the expected bones are not available, first verify that **Target Skeleton** is assigned to the correct Skeleton asset.
