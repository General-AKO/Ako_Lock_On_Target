---
icon: window
---

# UI Target Info

> <mark style="color:orange;">**Development Note:**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">The Target UI system and its editor preview are still under development.</mark>&#x20;

The **UI Target Info** settings allow you to configure the UI that can be <mark style="color:$success;">displayed</mark> when a target is locked on.

The UI is configured through a <mark style="color:green;">**Target UI Data Asset**</mark>. This Data Asset contains the information used to define the type of Widget, its appearance, position, and other supported UI settings.

The Data Asset is divided into several sections.

***

## <mark style="color:$success;">1- Widget</mark>

The **Widget** section defines which type of Widget you want to use for the Target UI.

#### <mark style="color:blue;">1-1- Widget Type</mark>

There are two available Widget Types:

#### <mark style="color:red;">Custom Widget</mark>

**Use this option when you want to provide your own Widget.**

After selecting `Custom Widget`, the **Info Widget** property becomes available, allowing you to select the Widget Blueprint you want to use.

This gives you the freedom to create your own target information interface and use it with the Lock-On system.

> **Preview Note:** Custom Widgets are supported at runtime, but they are currently not displayed by the Target UI Preview.

***

#### <mark style="color:red;">Status Widget</mark>

**Use this option to use the Status Widget included with the system.**

After selecting `Status Widget`, the **Status Widget Class** property becomes available, allowing you to choose which supported Status Widget should be used.

You can also configure:

#### <mark style="color:red;">Status Widget Alignment</mark>

**Determines where the Status Widget is positioned relative to the target UI.**

You can choose to display it:

* **Top**
* **Bottom**
* **Left**
* **Right**

This allows you to control where the Status Widget appears around the main Target UI.

***

## <mark style="color:$success;">2- UI Target Info</mark>

The **UI Target Info** section controls how the Target UI is displayed and positioned.

#### <mark style="color:blue;">2-1- UI Mode</mark>

**Determines whether the Target UI is displayed as a&#x20;**<mark style="color:$success;">**normal screen UI**</mark>**&#x20;or as a&#x20;**<mark style="color:$success;">**World UI**</mark>**.**

You can choose between:

* **UI Normal** — Displays the Widget normally on the screen.
* **UI World** — Allows the Widget to be placed in the game world and provides additional world-space configuration.

When using `UI World`, additional settings become available to control the Widget's placement and appearance.

#### <mark style="color:red;">Widget Space</mark>

**Defines the space in which the Widget is displayed.**

You can choose between:

* **Screen** — The Widget is displayed in screen space.
* **World** — The Widget is displayed in world space.

#### <mark style="color:red;">UI Pivot</mark>

**Defines the pivot point used when positioning the Widget.**

This controls the point of the Widget that is used as the reference for its location.

#### <mark style="color:red;">UI Location</mark>

**Defines the Widget's position.**

The effect of this setting depends on the selected Widget Space and allows you to control where the UI appears.

#### <mark style="color:red;">UI Rotation</mark>

**Defines the rotation of the Widget.**

This allows you to control the orientation of the Target UI.

#### <mark style="color:red;">UI Scale</mark>

**Defines the scale of the Widget.**

Use this to make the Target UI larger or smaller.

#### <mark style="color:red;">UI Draw Size</mark>

**Defines the draw size of the Widget.**

This controls the size used when rendering the Widget, particularly when working with World Space UI.

#### <mark style="color:red;">UI Geometry Mode</mark>

**Defines how the Widget geometry is handled when displayed in World Space.**

This setting is useful when configuring how the World UI is represented in the game world.

#### <mark style="color:red;">UI Face Camera</mark>

**Makes the World Space Widget continuously face the player's camera.**

This option is only available when **Widget Space** is set to **World**.

When enabled, the Widget automatically rotates to face the player's view, making it easier to keep the Target UI readable while moving around the target.

***

## <mark style="color:$success;">3- Status Elements</mark>

When **Widget Type** is set to **Status Widget**, an additional **Status Elements** section becomes available.

This section allows you to customize how the status information is visually displayed inside the Status Widget.

#### <mark style="color:$warning;">Status Display Mode</mark>

**Defines the overall visual layout used for the status element.**

There are two display modes:

* **Progress Bar Style** — Displays the progress bar with optional status text.
* **Progress Bar & Status Style** — Displays the progress bar together with status text inside a styled panel and enables additional background and border customization.

#### <mark style="color:$warning;">Display Style</mark>

**Defines how the status value itself is displayed.**

You can choose from:

* **Simple Progress Bar** — Uses a standard progress bar.
* **Custom Progress Bar** — Uses the custom segmented progress bar style.
* **Text** — Displays the status as text without using a progress bar.

#### <mark style="color:red;">Segment Count</mark>

**Defines the number of visual segments used to represent the full status value.**

This option is available when **Custom Progress Bar** is selected.

For example, with a segmented or star-shaped progress bar and a Segment Count of **10**:

* **100%** = 10 segments
* **50%** = 5 segments

This only changes how the value is visually represented. It does **not** change the actual status value.

#### <mark style="color:$warning;">Fill Color and Opacity</mark>

**Defines the color and opacity of the progress indicator.**

This setting is available when a progress bar style is being used.

#### <mark style="color:$warning;">Progress Bar Image</mark>

**Defines the image used for the visual appearance of the progress bar.**

This allows you to customize the look of the progress bar instead of relying on a default appearance.

#### <mark style="color:$warning;">Progress Bar Size</mark>

**Defines the size of the progress bar.**

* **X** = Width
* **Y** = Height

#### <mark style="color:$warning;">Opacity Noise</mark>

**Controls the visibility of the noise effect applied to the progress bar.**

Higher values make the noise effect less noticeable, while lower values make it more noticeable.

#### <mark style="color:$warning;">Strength Noise</mark>

**Controls the amount of detail visible in the noise effect.**

Lower values produce less visible noise detail.

A value of **0** completely hides the effect.

#### <mark style="color:$warning;">Status Text</mark>

**Defines the text displayed for the status element.**

Use this to provide a label or name for the displayed status.

#### <mark style="color:$warning;">Status Text Color</mark>

**Defines the color of the Status Text.**

#### <mark style="color:$warning;">Status Text Font</mark>

**Defines the font and text properties used by the Status Text.**

***

### <mark style="color:purple;">Text Display Settings</mark>

When **Display Style** is set to **Text**, additional settings become available for configuring the text-based status display.

#### Description Text

**Defines the additional descriptive text displayed with the status.**

This can be used to provide more context about what the displayed value represents.

#### Description Text Color

**Defines the color of the Description Text.**

#### Description Text Font

**Defines the font and text properties used by the Description Text.**

#### Auto Wrap Text

**Automatically wraps the Description Text when it reaches the available space.**

This is useful when the description is longer than the available UI width and should continue on additional lines instead of extending beyond the Widget.
