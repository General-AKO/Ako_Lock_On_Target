# Multiple Status Elements

You can combine several Status Elements in the same Target UI Data Asset.

Example:

```text
Boss Target UI
├── Health      → Custom Progress Bar
├── Shield      → Simple Progress Bar
└── Phase       → Text
```

This lets one target panel present several independent values without creating a separate Data Asset for each value.

A good approach is to keep each element focused on one gameplay concept and use a shared Data Asset whenever the same layout is reused across multiple targets.
