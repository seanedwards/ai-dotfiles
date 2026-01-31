---
name: configuring-niri
description: Use when configuring Niri window manager, writing niri config files, setting up keybindings, window rules, animations, or troubleshooting Niri issues - navigates comprehensive reference documentation
---

# Configuring Niri

Niri is a scrollable-tiling Wayland compositor. This skill navigates the complete Niri documentation to answer configuration questions.

**Config location:** `~/.config/niri/config.kdl` (KDL syntax, live-reloaded)

**Commands:** `niri validate` (check config) | `niri msg action reload-config` (force reload)

## How to Use This Skill

1. Identify user intent from the topic index below
2. Read the relevant doc file(s) from the `docs/` subdirectory (paths are relative to this skill's directory)
3. Answer using the documentation content

**Always read docs before answering** - don't rely on general knowledge about Niri.

## Topic Index

### Configuration Sections (config.kdl blocks)

| User asks about... | Read this file | Config block |
|--------------------|----------------|--------------|
| Keyboard shortcuts, hotkeys, binds | `docs/Configuration:-Key-Bindings.md` | `binds {}` |
| Mouse, touchpad, tablet, sensitivity | `docs/Configuration:-Input.md` | `input {}` |
| Monitors, displays, resolution, scale | `docs/Configuration:-Outputs.md` | `output "name" {}` |
| Window gaps, columns, sizing, borders | `docs/Configuration:-Layout.md` | `layout {}` |
| Per-app settings, opacity, floating | `docs/Configuration:-Window-Rules.md` | `window-rule {}` |
| Animations, easing, duration | `docs/Configuration:-Animations.md` | `animations {}` |
| Touchpad/touchscreen gestures | `docs/Configuration:-Gestures.md` | `gestures {}` |
| Layer shell, panels, bars | `docs/Configuration:-Layer-Rules.md` | `layer-rule {}` |
| Named/persistent workspaces | `docs/Configuration:-Named-Workspaces.md` | `workspace {}` |
| Lid close, tablet mode switch | `docs/Configuration:-Switch-Events.md` | `switch-events {}` |
| Alt-tab, window switching | `docs/Configuration:-Recent-Windows.md` | `recent-windows {}` |
| Config splitting, modular config | `docs/Configuration:-Include.md` | `include "file"` |
| Debug, render, damage tracking | `docs/Configuration:-Debug-Options.md` | `debug {}` |
| Top-level flags (prefer-no-csd, etc) | `docs/Configuration:-Miscellaneous.md` | (top level) |

### Usage & Concepts

| User asks about... | Read this file |
|--------------------|----------------|
| Installation, first setup, dependencies | `docs/Getting-Started.md` |
| How workspaces work, workspace navigation | `docs/Workspaces.md` |
| Floating windows, how to float | `docs/Floating-Windows.md` |
| Tabs, tabbed windows | `docs/Tabs.md` |
| Fullscreen, maximize behavior | `docs/Fullscreen-and-Maximize.md` |
| Gestures overview (not config) | `docs/Gestures.md` |
| Screen recording, OBS, pipewire | `docs/Screencasting.md` |
| IPC, niri msg, scripting | `docs/IPC.md` |
| Systemd integration, autostart | `docs/Example-systemd-Setup.md` |
| Status bars, launchers, notifications | `docs/Important-Software.md` |
| Layer shell panels (waybar, etc) | `docs/Layer‐Shell-Components.md` |

### Troubleshooting

| User asks about... | Read this file |
|--------------------|----------------|
| Common questions, how to X | `docs/FAQ.md` |
| App-specific problems (Electron, etc) | `docs/Application-Issues.md` |
| X11 apps, Steam, games, XWayland | `docs/Xwayland.md` |
| Nvidia GPU issues | `docs/Nvidia.md` |
| Fractional scaling issues | `docs/Fractional-Layout.md` |
| Accessibility, screen readers | `docs/Accessibility.md` |

### Development (rarely needed)

| Topic | File |
|-------|------|
| Contributing to niri | `docs/Development:-Developing-niri.md` |
| Design philosophy | `docs/Development:-Design-Principles.md` |
| Animation internals | `docs/Development:-Animation-Timing.md` |

### Examples

Shader examples for animations: `docs/examples/`

## Keyword Quick Reference

Common search terms → doc file:

- **rounded corners, corner radius** → `Configuration:-Window-Rules.md`
- **CSD, client-side decorations** → `Configuration:-Miscellaneous.md` + `FAQ.md`
- **blur** → `FAQ.md` (not yet supported)
- **sticky, pinned, always on top** → `FAQ.md` (not yet supported)
- **hotkey overlay, startup popup** → `FAQ.md`
- **focus ring, border color** → `Configuration:-Layout.md`
- **spawn, exec, run command** → `Configuration:-Key-Bindings.md`
- **screenshot** → `Configuration:-Key-Bindings.md` (look for screenshot action)
- **natural scroll, tap to click** → `Configuration:-Input.md`
- **HiDPI, 4K, scaling** → `Configuration:-Outputs.md`
- **VRR, variable refresh** → `Configuration:-Outputs.md`
