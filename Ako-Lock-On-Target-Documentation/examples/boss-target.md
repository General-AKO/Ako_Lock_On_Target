# Boss Target

A boss often benefits from a dedicated UI Data Asset because the presentation may contain several independent status values.

Example asset structure:

```text
DA_Target_Enemy
DA_Target_Boss
```

The boss Data Asset can contain multiple status elements such as:

- Health
- Shield
- Phase

Create the separate asset when you want boss-specific UI changes to remain isolated from the standard enemy presentation.
