# Game Clean Architecture - Component Creator

Boilerplate generator for game components following Clean Architecture principles, supports multiple game engines.

## Features

- Automatically creates folder structure and files for new game components
- Generates Clean Architecture structure (Domain, View, Presenter, Factory, Test)
- Supports multiple engines

## Supported engines

- Unity
- Godot (Mono/C#)

## Prerequisites

- Python installed globally on your system

## Engine-Specific Requirements

| Feature | Unity | Godot |
|---------|-------|-------|
| Test Framework | NUnit | GdUnit4 |

## Installation

1. Copy the `create.py` script to your project's components root folder (e.g., `Assets/MyCoolGame` for Unity)
2. Ensure you have execution permissions for the script

## Usage

Run the script from the command line with the following arguments:

```bash
python create.py <ComponentName> <ProjectName> <Engine>
```

### Arguments

- `ComponentName`: The name of your new component (e.g., "Player", "Inventory")
- `ProjectName`: Your project's namespace (e.g., "MyCoolGame")
- `Engine`: Either "Unity" or "Godot"

### Example

```bash
python create.py Player MyCoolGame Unity
```

## Generated Structure

- **Domain**: Contains the core business logic
- **View**: Handles the bridge between domain and presentation logic
- **Adapter**: Defines the interface between View and engine-specific implementation
- **Factory**: Creates and manages component instances
- **Tests**: Contains unit tests for the component
- **Engine-Specific**: Contains platform-specific implementations

## Future Improvements

- [ ] Create installer for global command execution
- [ ] Add package support (UPM for Unity, Asset Library for Godot)
- [ ] Add configuration files for template customization

## Contributing

Feel free to open issues or submit pull requests for improvements.

## License

[Add your chosen license here]