---
icon: kitchen-set
---

# Target UI & Widget Control

> #### <mark style="color:green;">The system allows you to go beyond the default Target UI and directly control the Widget used by your target.</mark>

> #### <mark style="color:green;">You can use your own</mark> <mark style="color:green;"></mark><mark style="color:green;">**Custom Widget**</mark> <mark style="color:green;"></mark><mark style="color:green;">or the built-in</mark> <mark style="color:green;"></mark><mark style="color:green;">**Status Widget**</mark><mark style="color:green;">, then access its reference from Blueprint to update Health, Stamina, Shield, or any other values you want to display.</mark>

A complete example of this workflow is already included in <mark style="color:$success;">**`BP_NPC_CHARACTER`**</mark>.

### <mark style="color:blue;">1- Using the Built-In Status Widget</mark>

When using the **Status Widget** provided with the system, you can update its progress values using:

#### Update Progress Bar Value

**Updates the value displayed by a Progress Bar inside the Status Widget.**

It provides:

* **Percent** — The value to display, from **0 to 1**.
* **Percent Index** — Selects which Progress Bar should be updated when the Widget contains multiple bars.

For example:

```
0.0 = 0%
0.5 = 50%
1.0 = 100%
```

This can be used for Health, Stamina, Shield, or any other status represented by a progress bar.

<figure><img src="../../../../.gitbook/assets/Cap 2026-10-07 10-21-42.jpg" alt=""><figcaption></figcaption></figure>

***

### <mark style="color:$success;">2- Getting Your Widget Reference</mark>

When using your own <mark style="color:$danger;">**Custom Widget**</mark>, or when you need direct access to a Widget's variables and functions, the system provides a helper Macro called:

#### <mark style="color:green;">Get Widget Ref</mark>

**Use this Macro to obtain a reference to the Target UI Widget and update it from your own Blueprint logic.**

The Macro is designed to work directly with **Event Tick**. It gets the Widget reference only once when the Widget becomes visible, then allows your update logic to run every frame while the Widget remains visible.

This means you do not need to manually rebuild the Widget reference logic yourself.

<figure><img src="../../../../.gitbook/assets/Cap 2026-10-07 10-24-45.jpg" alt=""><figcaption></figcaption></figure>

#### <mark style="color:red;">Do Your Cast</mark>

Use **Do Your Cast** to Cast the Widget to your own Widget class.

After the Cast succeeds, store the result in a variable. You can then use that reference to access the Widget's own variables and functions.

The Widget used as the Cast Object comes from:

**`NPC UI Info Array Valide`**

If the target has multiple Widgets, use the corresponding Array Index:

```
Index 0 → First Widget
Index 1 → Second Widget
Index 2 → Third Widget
```

#### <mark style="color:red;">Apply Logic</mark>

Use **Apply Logic** for the logic that should update your Widget while it is visible.

After creating your Widget reference, use **Is Valid** to make sure the reference is available, then apply any changes you need.

For example, you can update:

* Health
* Stamina
* Shield
* Status values
* Custom Widget variables
* Any other information exposed by your Widget

#### <mark style="color:red;">NPC UI Info Array Valide</mark>

**`NPC UI Info Array Valide`** provides the valid Target UI Widget references currently available for the target.

Use its Array Index to access the specific Widget you want to Cast.

***

### <mark style="color:$success;">Reusing the Helper</mark>

The **Get Widget Ref** Macro is designed to be reusable.

After understanding the setup, you can copy the Macro into your own character and use the same workflow to access and update your Target UI Widgets.

For a ready-to-use example, check **`BP_NPC_CHARACTER`** included with the Demo.
