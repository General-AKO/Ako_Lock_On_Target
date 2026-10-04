---
icon: magnifying-glass-chart
---

# overview

> #### The Lock-On Target system uses <mark style="color:$success;">**two different settings components**</mark>, each serving a different purpose depending on where you want to configure the system.

— The first is <mark style="color:$primary;">**`Ako_LockOnTarget`**</mark>, which is an **Actor Component** added to the **Player Character**. It contains the general Lock-On settings used by the system.

<figure><img src="../.gitbook/assets/Screenshot 2026-10-04 130241.png" alt=""><figcaption></figcaption></figure>

— The second is <mark style="color:purple;">**`Cus_Setting`**</mark>, which is added to the **Target Actor**. It provides <mark style="color:green;">additional settings</mark> that allow you to customize how a specific target behaves when it is used by the Lock-On system.

<figure><img src="../.gitbook/assets/Screenshot 2026-10-04 130320.png" alt=""><figcaption></figcaption></figure>

For example, you can use <mark style="color:$success;">**`Cus_Setting`**</mark> when you want a specific target to:

* Display a custom Widget when it becomes locked on.
* Use a custom Target Icon.
* Change the icon Lock-On location.
* Apply other target-specific customization.

## <mark style="color:cyan;">How</mark> <mark style="color:cyan;"></mark><mark style="color:cyan;">`Cus_Setting`</mark> <mark style="color:cyan;"></mark><mark style="color:cyan;">Works</mark>

`Cus_Setting` is an **optional customization layer** for individual targets. It does not replace the main Lock-On settings.

— When a target <mark style="color:$danger;">does not have</mark> a `Cus_Setting` component, the system simply uses the <mark style="color:$success;">**general settings configured**</mark>**&#x20;in `Ako_LockOnTarget`**.

— When `Cus_Setting` is present on the target, the system can use its <mark style="color:$success;">additional settings</mark> to customize that target according to your configuration.

This gives you a simple way to keep common behavior in `Ako_LockOnTarget` while customizing individual targets <mark style="color:orange;">only when needed</mark>.

> #### <mark style="color:yellow;">The following sections explain how to use and configure both</mark> <mark style="color:yellow;"></mark><mark style="color:yellow;">**`Ako_LockOnTarget`**</mark> <mark style="color:yellow;"></mark><mark style="color:yellow;">and</mark> <mark style="color:yellow;"></mark><mark style="color:yellow;">**`Cus_Setting`**</mark><mark style="color:yellow;">.</mark>
