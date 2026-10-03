# Responsibilities & Data Flow

A healthy integration keeps each layer responsible for the information it actually owns.

| Responsibility | Typical owner |
|---|---|
| Target configuration | Lock-On Target component |
| Target point configuration | Target component + lock-on Blueprint logic |
| Target icon configuration | Target component |
| Reusable UI definition | Target UI Data Asset |
| UI appearance | Custom Widget Blueprint or Status Widget Blueprint |
| Health / stamina / shield values | Project gameplay / Blueprint logic |
| Target selection / input | Project gameplay / lock-on logic |
| Editor preview | Plugin editor module + preview Blueprint |

## Why this separation matters

The plugin remains independent from a specific gameplay framework. Your game can decide how targets are acquired, how input works, where gameplay values come from, and how custom UI reacts to that data.

## Runtime values

The Status Widget base exposes runtime-facing status values, including a percentage value and an index value. Your Blueprint/gameplay implementation is responsible for supplying those values from your project's gameplay data.

The plugin therefore does not assume that "health" must come from a particular component, attribute system, or framework.
