# Game Clean Architecture - Component Creator

Code generator for game components following Clean Architecture principles.

## Features

- Automatically creates folder structure and files for new game components
- Generates Clean Architecture structure (Domain, View, Presenter, Factory, Test, etc)
- Supports multiple engines

## Supported engines

- Unity
- Godot (C#)

## Prerequisites

- Python 3.6 or newer

## Engine-Specific Requirements

| Feature | Unity | Godot |
|---------|-------|-------|
| Test Framework | NUnit | [GdUnit4](https://github.com/MikeSchulze/gdUnit4) |

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
- **Tests**: Test coverage: is the domain logic working and being presented as expected?

## Architecture Overview
This is my clean, decoupled architecture for game development. It follows SOLID principles and clean architecture patterns. It separates business logic from engine implementations while remaining pragmatic and maintainable. It allows me to properly cover my core logic with tests - if needed I could even port my game between engines while preserving most of the game logic. Feel free to use this as inspiration and adapt it to your needs - there are many valid approaches to game architecture.

![Component Creator Logo](architecture-diagram.jpg)

## Future Improvements

- [ ] Create installer for global command execution
- [ ] Add package support (UPM for Unity, Asset Library for Godot)
- [ ] Add configuration files for template customization

## Contributing

Feel free to open issues, submit pull requests for improvements and share your takes on game architecture.