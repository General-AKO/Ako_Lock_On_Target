# Blueprint Integration

The plugin provides the reusable C++ foundation for target configuration, target UI Data Assets, Status Widget support, and editor customization. Your Blueprint/gameplay layer can then decide how the system behaves in your project.

## Typical responsibility split

| Feature | Where it is typically implemented |
|---|---|
| Target actor configuration | Lock-On Target component |
| Target-point data | Target component |
| Target selection | Your lock-on/gameplay Blueprint logic |
| Input handling | Your gameplay/input setup |
| Camera behavior | Your project's camera / lock-on logic |
| Health, stamina, shield, etc. | Your gameplay systems |
| UI visual design | Widget Blueprint |
| Reusable UI settings | Target UI Data Asset |
| Editor preview | Plugin editor module + preview Blueprint |

## Keep gameplay data separate

The Data Asset describes presentation. It should not be treated as the authoritative source of live health, stamina, shield, or other gameplay state.

Your Blueprint logic should feed runtime values into the selected widget according to your project's own data model.

## Status Widget values

The Status Widget base exposes runtime-facing properties for status display, including a percentage value and an index value. Connect these values to the gameplay data that should be represented by each status element.

## Why this architecture is useful

The same documentation and UI definition can support many gameplay implementations because the plugin does not require one universal controller, camera, attribute, or health architecture.
