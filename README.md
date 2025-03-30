# Game Clean Architecture - Component Creator

Code generator for game components following Clean Architecture principles. Supports multiple game engines.

## Features

- Automatically creates folder structure and files for new game components
- Generates Clean Architecture structure (Domain, View, Presenter, Factory, Test)
- Supports multiple engines

## Supported engines

- Unity
- Godot (C#)

## Prerequisites

- Python 3.6 or newer

## Engine-Specific Requirements

| Feature | Unity | Godot |
|---------|-------|-------|
| Test Framework | NUnit | GdUnit4 |

## Installation

1. Copy the `create.py` script to your project's components root folder (`Assets` for Unity, `res://` for Godot)

## Usage

Run the script from the command line with the following arguments:

```bash
python create.py <ComponentName> <ProjectName> <Engine>
```

### Arguments

- `ComponentName`: The name of your new component (e.g., "Player", "Inventory")
- `ProjectName`: Your project's namespace (e.g., "MyCoolGame")
- `Engine`: One of the [Supported engines](#supported-engines)

### Example

```bash
python create.py Player MyCoolGame Unity
```

## Generated Structure

- **Domain**: Core business logic: how the game should behave?
- **View**: Bridge between domain and engine: how should the game be shown?
- **Adapter**: Interface for engine-specific implementation: what should the engine provide?
- **Engine-Specific**: Platform-specific implementations: how the adapter is implemented on the engine?
- **Factory**: Dependency injection and creation: what does the component require?
- **Tests**: Test coverage: is the domain logic working and being presented to the user?


## Future Improvements

- [ ] Create installer for global command execution
- [ ] Add package support (UPM for Unity, Asset Library for Godot)
- [ ] Add configuration files for template customization

## Contributing

Feel free to open issues or submit pull requests for improvements.