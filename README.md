---
cover: .gitbook/assets/lockon_icon.png
coverY: 505.62295081967216
---

# 🎯 ako Lock On Target

A <mark style="color:green;">**flexible**</mark>**&#x20;**<mark style="color:$success;">**combat targeting framework**</mark> for Unreal Engine that brings together lock-on, target interaction, target management, and customizable combat UI in a reusable system designed to integrate with a <mark style="color:green;">**wide variety**</mark> of <mark style="color:$success;">**gameplay**</mark> experiences.

<figure><img src=".gitbook/assets/lockon_icon.png" alt=""><figcaption></figcaption></figure>

### <mark style="color:$success;">What this documentation covers</mark>

This documentation is written for users interesting about **ADVANCED TARGETING SYSTEM & COMBAT INTERACTION SYSTEM** into an Unreal Engine project.

It covers everything you need to understand, configure, and use the system—from the main Lock-On setup and target selection to directional and bone-based targeting, target-specific customization, Target UI, combat interactions, Motion Warping, Blueprint Functions and Events, and the included Demo.

The system is built around two main configuration layers:

* <mark style="color:$success;">**`Ako_LockOnTarget`**</mark> — An Actor Component added to your Player Character. It contains the main settings that control the overall targeting and combat behavior.
* <mark style="color:$success;">**`Cus_Setting`**</mark> — An optional component added to individual targets. It provides additional target-specific customization such as Lock-On points, target bones, icons, and Target UI behavior.

Your own Blueprint/gameplay logic can then use the system's **Functions, Events, and Inputs** to connect targeting and combat behavior to the rest of your game.

## <mark style="color:$success;">Start here</mark>

New to the system? Follow this path:

1. [TEST THE PROJECT DEMO](example-content.md)
2. [FIRST AND LAST STEP](setting-up-the-plugin/first-and-last-step.md)
3. [Lock-On component Settings](https://app.gitbook.com/s/gcOIcK1ffuaNksbK8Dpz/lock-on-component-settings)

