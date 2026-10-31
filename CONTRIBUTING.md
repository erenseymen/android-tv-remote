# Contributing to TV Remote

Thank you for your interest in contributing to TV Remote! This document provides guidelines for contributing to the project.

## Development Setup

### Prerequisites

- Linux with Flatpak support
- `flatpak` and `flatpak-builder` installed
- GNOME SDK runtime: `org.gnome.Sdk//51`

### Building

```bash
# Build and install the Flatpak
./build-and-run.sh
```

Or manually:

```bash
flatpak-builder --user --install --force-clean build-dir flatpak/io.github.erenseymen.android-tv-remote.yml
flatpak run io.github.erenseymen.android-tv-remote
```

## Code Style

- Python code follows PEP 8 guidelines
- Use type hints for all function parameters and return values
- All modules should have docstrings explaining their purpose
- Use `from __future__ import annotations` for modern type hint syntax

## Pull Request Process

1. **Open an issue first** to discuss the proposed change
2. Fork the repository and create a feature branch
3. Make your changes with clear, descriptive commit messages
4. Ensure the application builds and runs correctly
5. Submit a pull request with a clear description of the changes

## Reporting Issues

When reporting issues, please include:

- Your Linux distribution and version
- Flatpak version
- Steps to reproduce the issue
- Expected vs actual behavior
- Any relevant error messages (check `flatpak run --command=sh io.github.erenseymen.android-tv-remote` for logs)

## Code Organization

- **`src/gnome_adb_tv_remote/core/`** - Core logic (ADB, networking, scrcpy)
- **`src/gnome_adb_tv_remote/ui/`** - GTK4/Libadwaita UI components
- **`data/`** - Desktop files, icons, and GSettings schema
- **`flatpak/`** - Flatpak build manifest

## License

By contributing, you agree that your contributions will be licensed under the GPL-3.0-or-later license.
