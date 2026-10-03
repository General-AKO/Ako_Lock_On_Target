# Bone-Based Targeting

Use this setup when the active lock-on point should move between meaningful locations on the target.

## Configuration

1. Assign **Target Skeleton**.
2. Select **Switch Between Bones**.
3. Add the required bones to **Lock On Target Bones**.
4. Enable **Use Bone Icon Target** when each bone should use a dedicated icon.
5. Leave Bone Icon empty on entries that should use the default Lock On Icon.
6. Enable **Follow Target Point** when the UI should move with the active bone.

Example:

```text
Head      → Head marker
Chest     → Default marker
Left Arm  → Arm marker
Right Arm → Arm marker
```

The target actor remains the same target while the active point can change between the configured bones according to your lock-on Blueprint logic.
