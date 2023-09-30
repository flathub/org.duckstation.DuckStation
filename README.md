# Flatpak for DuckStation

NOTE: The manifest and XML in this repository are automatically generated, see https://github.com/stenzek/duckstation/blob/master/scripts/flatpak/update-flathub.sh

Please do not submit Pull Requests, as any changes will get lost on next update.

## Installation

1. [Set up Flatpak](https://www.flatpak.org/setup/)

2. Install DuckStation from [Flathub](https://flathub.org/apps/details/org.duckstation.DuckStation)

`flatpak install -y org.duckstation.DuckStation`

3. Run DuckStation

`flatpak run org.duckstation.DuckStation`

To uninstall: `flatpak uninstall -y org.duckstation.DuckStation`

## Build

The `flatpak-builder` package is required.

- Install the SDK

`flatpak install org.kde.Platform/x86_64/6.5 org.kde.Sdk/x86_64/6.5 org.freedesktop.Sdk.Extension.llvm16`

- Build DuckStation

`flatpak-builder --user --install --force-clean build-dir org.duckstation.DuckStation.json`
