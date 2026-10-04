---
icon: sparkles
---

# Character Setting

> <mark style="color:$warning;">The</mark> <mark style="color:orange;">**Character Setting**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">section is used to define the skeletal setup of the target when the target uses a</mark> <mark style="color:orange;"></mark><mark style="color:orange;">**Skeletal Mesh**</mark><mark style="color:orange;">.</mark>

If your target does not have a skeletal structure, you can leave these settings unused.

#### Target Skeleton

**Specify the Skeletal Skeleton used by the target.**

Select the Skeleton that belongs to the **Skeletal Mesh used by this Target Actor**.

> <mark style="color:$danger;">**Important:**</mark> <mark style="color:$danger;"></mark><mark style="color:$danger;">Make sure you select the correct Skeleton.</mark>\ <mark style="color:$danger;">Do not assign a Skeleton from another character or target. The selected Skeleton must belong to the Skeletal Mesh actually used by the Target Actor.</mark>

Once a valid Skeleton is assigned, the system provides the following information:

#### <mark style="color:blue;">--Lock On Target Bones</mark>

**Displays the bones available in the assigned Skeleton.**

This is a read-only list generated automatically from the selected Skeleton. You do not manually add or remove bones from this list.

The list represents the bones that the system can retrieve from the target's skeletal structure.

#### <mark style="color:blue;">--Target Bone</mark>

**Defines which bones should be used as Lock-On targets and allows you to assign a Target Icon to each one.**

This setting is an **Array of Maps**, where each entry contains the bone name and the icon associated with that bone.

You can use it to specify the specific bones you want players to be able to switch between during Lock-On, along with a different Target Icon for each bone when needed.

> <mark style="color:yellow;">**Note:**</mark> <mark style="color:yellow;"></mark><mark style="color:yellow;">You do not need to assign an icon to every bone.</mark>\ <mark style="color:yellow;">If a bone does not have a specific icon assigned, the system will automatically use the general</mark> <mark style="color:yellow;"></mark><mark style="color:yellow;">**Lock On Icon**</mark> <mark style="color:yellow;"></mark><mark style="color:yellow;">instead.</mark>

For example, if you want to use **the same Target Icon for every bone**, you do not need to configure individual icons here. Simply leave the bone icons unchanged and set the general **Lock On Icon** from the Ako\_LockOnTerget setting.

> <mark style="color:orange;">**Important:**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">The bones configured here are not used for bone switching unless</mark> <mark style="color:orange;"></mark><mark style="color:orange;">**Switch Between Bone**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">is selected in</mark> <mark style="color:orange;"></mark><mark style="color:orange;">**Target Point Loc**</mark><mark style="color:orange;">.</mark>

This allows you to keep the default setup simple and only configure individual target bones when you actually need bone switching.
