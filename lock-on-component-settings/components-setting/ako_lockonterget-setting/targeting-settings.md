# Targeting Settings

The **Targeting Settings** section contains the main settings that control how the Lock-On Target system detects, selects, switches, and maintains targets.

These settings determine which Actors can be considered as targets, how far the system searches, how targets are selected, and when the Lock-On should be maintained or cancelled.

#### Target Object Types

**Use this setting to define which Object Types the Lock-On system can interact with.**

Any Actor using one of the selected Object Types can be considered a potential Lock-On Target.

By default, this is set to **Pawn**, meaning Actors using the Pawn Object Type can be detected as potential targets.

You can add **multiple Object Types** when your project requires the system to recognize different types of Actors as valid targets.

***

#### Detection Radius

**Defines the radius of the area used to search for potential targets.**

Actors located inside this detection area can be considered by the Lock-On system and then evaluated by the other targeting checks.

A larger radius allows the system to search a wider area around the player, while a smaller radius limits the search area.

***

#### Detection Distance

**Defines how far forward the detection trace extends when searching for targets.**

This controls the forward reach of the targeting detection and works together with the Detection Radius to determine the area in which potential targets can be found.

***

#### Max Lock On Distance

**Defines the maximum distance a target can be from the player while remaining locked on.**

When the currently locked target moves beyond this distance, the Lock-On will be broken and the target will be unlocked.

This setting controls the distance at which an already selected target can no longer be maintained.

***

#### Check Obstruction OnTarget

**Checks whether the current target is obstructed by another object, such as a wall or other obstacle.**

When the target is blocked from the player, it cannot be selected or switched to.

> **Important:** For the current version, it is recommended to keep this option **enabled at all times**.

***

#### Check Obstruction OnBone

**Checks whether the currently selected target bone is obstructed by another object.**

If the selected bone is blocked, that bone cannot be used as the active Lock-On point. This also prevents targets or target points that are behind an obstacle from being switched to.

This setting is particularly relevant when using the system's **Target Bone Switching** functionality.

***

#### Use Switch Based On Real Position

**Determines how the system chooses a new target when switching between targets using left/right directional input.**

When enabled, target switching is based on the target's **actual world position**.

For example, when switching to the right, the system looks for a suitable target that is physically located to the right of the current target in the game world.

When disabled, switching is based on the target's **screen position relative to the camera**. In this case, the system considers whether a target appears to the left or right on the screen, regardless of its actual world position.

This option lets you choose whether directional target switching should follow the **physical world position** of targets or how they **appear on screen**.

***

#### Target Icon Size

**Defines the size of the Target Icon displayed on a locked target.**

This value controls the base size of the icon when it is displayed.

Individual targets can override this value through their own **`Cus_Setting`** configuration when you want a specific target to use a different icon size.

***

#### Icon Target

**Defines the default icon displayed on a target when it is locked on.**

This icon is used by default for targets that do not provide their own custom icon.

You can override this setting for individual targets using **`Cus_Setting`**, allowing different targets to display different Lock-On icons.

***

#### Min Icon Target Scale

**Defines the minimum scale the Target Icon can reach as the distance from the target increases.**

As the target becomes farther away, the icon can scale down according to the system's distance-based scaling behavior. This setting defines the smallest scale the icon is allowed to reach.

* **Higher values** = The icon remains larger at greater distances.
* **Lower values** = The icon can become smaller at greater distances.

***

#### Auto Lock On Target

**Enables automatic target selection.**

When enabled, the system can automatically select and lock onto a target without requiring you to manually trigger the normal Lock-On selection.

The automatic selection behavior can select a target based on the targeting method configured for your system, such as prioritizing the target closest to the camera or the target toward which the camera is moving.

This option is useful when you want the Lock-On system to acquire targets automatically instead of waiting for manual target selection.

***

#### Time to Unlock on Lost Target

**Defines how long the system should wait before unlocking a target after its visibility is lost.**

For example, when a wall or another obstacle blocks the current target, the Lock-On does not have to be removed immediately. The system waits for the specified amount of time while the obstruction remains.

If the target is still obstructed after this delay, the Lock-On is cancelled and the target is unlocked.

This allows you to prevent the Lock-On from being lost instantly when the target is only briefly hidden.

***

#### Use Desired Rotation

**Determines which character rotation method is used while the Lock-On system controls rotation.**

When enabled, the system uses **Desired Rotation**.

When disabled, the system uses **Orient Rotation**.

Use the option that matches the rotation setup and behavior of your character.

***

#### Enable Stable Camera

**Determines how the camera behaves while Lock-On is active.**

When enabled, the camera remains **completely fixed** while the player is locked onto a target.

When disabled, the camera uses **smooth movement** while tracking the target, allowing it to adjust naturally during Lock-On.

This gives you the choice between a fully stable camera and a smoother camera-tracking behavior.
