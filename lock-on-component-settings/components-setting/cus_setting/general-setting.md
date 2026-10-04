---
icon: hubspot
---

# General Setting

> #### <mark style="color:yellow;">**The General Setting section contains the main settings used to customize the Lock-On point and determine where the Target Icon is displayed on the target.**</mark>

### <mark style="color:$success;">1- Target Point Loc</mark>

**Defines the Lock-On point used to determine where the Target Icon is displayed on the target.**

You can choose from <mark style="color:$success;">**four**</mark> different methods:

#### <mark style="color:cyan;">**1-1- Default**</mark>

**Uses the&#x20;**<mark style="color:pink;">**center**</mark>**&#x20;of the target as the Lock-On point.**

The system automatically uses the target's center position to display the **Target Icon**.

#### <mark style="color:cyan;">**1-2- Use Custom Z Height**</mark>

**Allows you to manually control the vertical position of the Lock-On point.**

The position is controlled using **`Custom Z Height`**, with a value ranging from **-1 to 1**.

* **1** — Top of the target
* **0** — Center of the target
* **-1** — Bottom of the target

Values between these points allow you to place the Lock-On point at different heights along the target.

#### <mark style="color:cyan;">**1-3- Use Specific Bone Location**</mark>

**Allows you to use a&#x20;**<mark style="color:red;">**specific bone**</mark>**&#x20;as the Lock-On point.**

This option requires the target to have a <mark style="color:$primary;">**Skeletal Mesh**</mark>. You can select the bone you want to use from <mark style="color:$success;">**`Selected Bone`**</mark>.

`Selected Bone` provides the available bones from the target's Skeleton, allowing you to choose a specific bone as the position used for the Lock-On Icon.

#### <mark style="color:cyan;">**1-4- Use Switch Between Bones**</mark>

**Allows the Lock-On point to dynamically switch between&#x20;**<mark style="color:orange;">**multiple target bones**</mark>**.**

When <mark style="color:$success;">enabled</mark>, the system selects the bone that is **closest to your current camera view direction**, using the same general logic used when selecting targets.

The active Lock-On point can then be switched between the configured target bones as you change your view.

The bones available for switching are taken from the <mark style="color:$success;">**`Lock On Target Bones`**</mark> list configured in the **Character Setting** section.

This option is useful when you want the Lock-On point to dynamically move between specific parts of a character instead of remaining fixed to a single location.
