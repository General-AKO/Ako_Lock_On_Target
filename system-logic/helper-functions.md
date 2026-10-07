# Helper Functions

The system provides a collection of Blueprint Functions and Helper Tools that allow you to access the current target, control Lock-On directly, work with target bones, retrieve target information, and interact with the Target UI.

<figure><img src="../.gitbook/assets/Cap 2026-10-03 13-57-47.jpg" alt=""><figcaption></figcaption></figure>

### <mark style="color:$success;">--Lock-On Control</mark>

#### <mark style="color:blue;">1- Get Current Target Lock On</mark>

**Returns a reference to the target currently locked on.**

Use this function whenever you need to access the active Lock-On Target in your own gameplay logic.

#### <mark style="color:blue;">2- Set Current Target</mark>

**Forces a specific target to become the current Lock-On Target.**

Instead of relying on the normal target selection system, you can use this function to directly specify which target should be locked onto.

#### <mark style="color:blue;">3- Reset Lock On</mark>

**Forces the Lock-On system to cancel the current target and exit Lock-On mode.**

Use this function when you want to manually perform an Unlock instead of waiting for the system to cancel the Lock-On automatically.

***

### <mark style="color:$success;">--Target Information</mark>

#### <mark style="color:blue;">4- Get Icon Target Size</mark>

**Returns the Target Icon size of the current target.**

Use this when you need the current target's configured icon size for your own UI or gameplay logic.

#### <mark style="color:blue;">5- Get Bone and Mesh Character</mark>

**Returns the current target's configured Lock-On Target Bones and its Skeletal Mesh.**

The **Lock-On Target Bones** output contains only the bones configured as selectable Lock-On targets. It does **not** represent the total number of bones in the Skeletal Mesh.

If the current target does not have a Skeletal Mesh, no skeletal data is returned. This does not mean the function has failed; the target simply has no skeletal structure to return.

***

### <mark style="color:$success;">-- Bone Targeting</mark>

#### <mark style="color:blue;">6- Find the Closest Bone to Camera View</mark>

**Finds the target bone closest to your current camera view direction.**

This function can be used **before Lock-On is activated**, making it useful when you want to determine which part of a target the player is looking at.

You can optionally provide a target manually using **Use Manual Target**.

It returns:

* **Bone Name** — The bone closest to the camera view.
* **Bone Location** — The world location of that bone.

Because the function performs additional calculations to determine the closest bone, avoid calling it continuously every frame through `Event Tick`.

For continuous checking, a delay of **0.1 seconds or more** is recommended.

#### <mark style="color:blue;">7- Get Current Target Mesh</mark>

**Returns information about a specified bone on the current target.**

Provide the bone name you want to check, and the function returns:

* **Is Valid** — Indicates whether the specified bone is valid.
* **Skeletal Mesh** — A reference to the target's Skeletal Mesh.
* **Socket Location** — The location of the specified bone when valid.

This function is particularly useful when working with the **Target Bone Switching** system and retrieving the Mesh associated with the current bone selection.

> **Important:** The Socket Location provided by this function is intended for the bone-switching workflow. It is not the general-purpose function for retrieving the current bone and its location in every situation.

For that purpose, use **Get Current Target Bone**.

#### <mark style="color:blue;">8- Get Current Target Bone</mark>

**Returns the currently active target bone and its location.**

Unlike `Get Current Target Mesh`, this function is designed to provide the current target bone information at any time, not only when switching between bones.

It returns:

* **Bone Name** — The currently active target bone.
* **Bone Location** — The current location of that bone.

If the current target does not have a Skeletal Mesh, the bone name returns **None**.

***

### <mark style="color:$success;">-- Animation Information</mark>

#### <mark style="color:blue;">9- Name Of The Current Active Montage</mark>

**Returns the name of the Animation Montage currently playing.**

Use this function when you need to identify the active montage in your own gameplay logic.

***

<figure><img src="../.gitbook/assets/Cap 2026-10-03 13-58-13.jpg" alt=""><figcaption></figcaption></figure>

***

## <mark style="color:$success;">Target Events</mark>

#### <mark style="color:blue;">1- On Target Change</mark>

**Triggered when the current Lock-On Target is switched to a new target.**

It provides:

* **New Target** — Reference to the new target.
* **Previous Target** — Reference to the target you were previously locked onto.
* **Current Bone** — The currently selected target bone, when available.

The bone name comes from the system's **Target Bone Switching** setup.

***

#### <mark style="color:blue;">2- On Target Unlock</mark>

**Triggered when the current Lock-On Target is unlocked.**

It provides:

* **Previous Target** — Reference to the last target that was locked on and has just been unlocked.

This allows you to react to the target being released while still having access to the last active target.

***

#### <mark style="color:blue;">3- First Target Lock</mark>

**Triggered when Lock-On is activated and the system acquires its first target.**

It provides:

* **Target** — Reference to the target that has been locked onto.
* **Current Bone** — The initially selected target bone, when available.

The bone is selected from the configured **Target Bone Switching** setup.

***

#### <mark style="color:blue;">4- On Target Bone Change</mark>

**Triggered when the active Lock-On point changes from one configured target bone to another.**

It provides:

* **Current Bone** — The newly selected bone.
* **Previous Bone** — The bone selected before the change.

The returned bones come from the configured **Target Bone Switching** setup.

***

#### <mark style="color:blue;">5- On Attack Start</mark>

**Triggered when a supported Lock-On attack montage starts.**

The Animation Montage must use **Motion Warping** with the Warp Target Name set to:

`LockOnAttack`

This allows the system to recognize the montage as a supported Lock-On attack and trigger the Event when the attack begins.

***

#### <mark style="color:blue;">6- On Attack End</mark>

**Triggered when a supported Lock-On attack montage ends.**

Like `On Attack Start`, the Animation Montage must use **Motion Warping** with the Warp Target Name:

`LockOnAttack`

This Event allows you to execute your own gameplay logic when the Lock-On attack finishes.

