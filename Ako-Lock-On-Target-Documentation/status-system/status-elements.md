# Status Elements

A **Status Widget** can contain multiple Status Elements. Each element represents one piece of target information with its own display configuration.

Example:

```text
Target UI
├── Health
├── Stamina
├── Shield
└── Status Text
```

## Status Display Mode

Each Status Element has a top-level display mode:

### Progress Bar Style

Focuses on the progress indicator itself and can include optional status text.

### Progress Bar & Status Style

Combines the progress indicator with status information in a styled panel. This mode makes panel-specific controls such as Background Color and Border Color relevant.

## Runtime data

The visual configuration does not define where the gameplay value comes from. Your Blueprint/gameplay logic supplies the runtime status values.
