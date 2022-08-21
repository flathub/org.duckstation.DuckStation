# Flatpak for DuckStation

## Installation

1. [Set up Flatpak](https://www.flatpak.org/setup/)

2. Install DuckStation from [Flathub](https://flathub.org/apps/details/org.duckstation.DuckStation)

`flatpak install -y org.duckstation.DuckStation`

3. Run DuckStation

`flatpak run org.duckstation.DuckStation`

On older hardware, adding `--env=MESA_GL_VERSION_OVERRIDE=4.2` may be needed to prevent it to crash at startup.

To uninstall: `flatpak uninstall -y org.duckstation.DuckStation`

## Build

The `flatpak-builder` package is required.

- Install the SDK

`flatpak install org.kde.Platform/x86_64/6.3 org.kde.Sdk/x86_64/6.3`

- Build Duckstation

`flatpak-builder --user --install --force-clean build-dir org.duckstation.DuckStation.yml`
