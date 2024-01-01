# Flatpak for DuckStation

> [!CAUTION]
> The manifest and metainfo in this repository are automatically generated from the upstream repository.
> 
> Please do not submit Pull Requests, they will be closed, as any changes will get lost on next update.
> 
> See https://github.com/stenzek/duckstation/blob/master/scripts/flatpak/update-flathub.sh.

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

`flatpak install org.kde.Platform/x86_64/6.6 org.kde.Sdk/x86_64/6.6 org.freedesktop.Sdk.Extension.llvm17`

- Build DuckStation

`flatpak-builder --user --install --force-clean build-dir org.duckstation.DuckStation.json`
