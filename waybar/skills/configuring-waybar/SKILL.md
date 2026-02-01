---
name: configuring-waybar
description: Use when configuring Waybar status bar, writing waybar config or style files, adding modules, styling with CSS, or troubleshooting Waybar issues - navigates comprehensive reference documentation
---

# Configuring Waybar

Waybar is a highly customizable Wayland bar for Sway and other wlroots-based compositors. This skill navigates the complete Waybar documentation to answer configuration questions.

**Config location:** `~/.config/waybar/config.jsonc` (JSON with comments) and `~/.config/waybar/style.css`

**Commands:** `waybar` (start) | `killall waybar && waybar &` (restart) | `waybar --help`

## How to Use This Skill

1. Identify user intent from the topic index below
2. Read the relevant doc file(s) from the `docs/` subdirectory (paths are relative to this skill's directory)
3. Answer using the documentation content

**Always read docs before answering** - don't rely on general knowledge about Waybar.

## Topic Index

### Core Documentation

| User asks about... | Read this file |
|--------------------|----------------|
| Installation, getting started | `docs/Installation.md` |
| Main config structure, bar settings | `docs/Configuration.md` |
| CSS styling, themes, customization | `docs/Styling.md` |
| Common problems, troubleshooting | `docs/FAQ.md` |
| All available modules overview | `docs/Modules.md` |
| Example configurations | `docs/Examples.md` |
| Available themes | `docs/Themes.md` |

### System Monitoring Modules

| User asks about... | Read this file | Module name |
|--------------------|----------------|-------------|
| CPU usage, load | `docs/Module:-CPU.md` | `cpu` |
| RAM, memory usage | `docs/Module:-Memory.md` | `memory` |
| Disk usage, mounts | `docs/Module:-Disk.md` | `disk` |
| System load averages | `docs/Module:-Load.md` | `load` |
| Temperature sensors | `docs/Module:-Temperature.md` | `temperature` |
| Battery status | `docs/Module:-Battery.md` | `battery` |
| Battery via UPower | `docs/Module:-UPower.md` | `upower` |
| Failed systemd units | `docs/Module:-Systemd-failed-units.md` | `systemd-failed-units` |

### Audio/Media Modules

| User asks about... | Read this file | Module name |
|--------------------|----------------|-------------|
| PulseAudio volume | `docs/Module:-PulseAudio.md` | `pulseaudio` |
| PulseAudio slider | `docs/Module:-PulseAudio-Slider.md` | `pulseaudio/slider` |
| WirePlumber/PipeWire | `docs/Module:-WirePlumber.md` | `wireplumber` |
| JACK audio | `docs/Module:-JACK.md` | `jack` |
| Sndio audio | `docs/Module:-Sndio.md` | `sndio` |
| MPD music player | `docs/Module:-MPD.md` | `mpd` |
| MPRIS media control | `docs/Module:-MPRIS.md` | `mpris` |
| Cava audio visualizer | `docs/Module:-Cava.md` | `cava` |
| Cava with GLSL shaders | `docs/Module:-Cava:-GLSL.md` | `cava` |
| Cava raw output | `docs/Module:-Cava:-Raw.md` | `cava` |

### Input/Display Modules

| User asks about... | Read this file | Module name |
|--------------------|----------------|-------------|
| Screen brightness | `docs/Module:-Backlight.md` | `backlight` |
| Brightness slider | `docs/Module:-Backlight-Slider.md` | `backlight/slider` |
| Keyboard state (caps, num) | `docs/Module:-Keyboard-State.md` | `keyboard-state` |
| Input language | `docs/Module:-Language.md` | `language` |
| Image display | `docs/Module:-Image.md` | `image` |
| Privacy indicators | `docs/Module:-Privacy.md` | `privacy` |

### Connectivity Modules

| User asks about... | Read this file | Module name |
|--------------------|----------------|-------------|
| Network status | `docs/Module:-Network.md` | `network` |
| Bluetooth | `docs/Module:-Bluetooth.md` | `bluetooth` |

### Workspace/Compositor Modules

| User asks about... | Read this file | Module name |
|--------------------|----------------|-------------|
| Generic workspaces | `docs/Module:-Workspaces.md` | `wlr/workspaces` |
| Sway workspaces, mode, window, scratchpad | `docs/Module:-Sway.md` | `sway/*` |
| Hyprland workspaces, window, submap | `docs/Module:-Hyprland.md` | `hyprland/*` |
| River tags, mode, window, layout | `docs/Module:-River.md` | `river/*` |
| Niri workspaces, window, language | `docs/Module:-Niri.md` | `niri/*` |
| Dwl tags, window | `docs/Module:-Dwl.md` | `dwl/*` |
| Taskbar (window list) | `docs/Module:-Taskbar.md` | `wlr/taskbar` |
| System tray | `docs/Module:-Tray.md` | `tray` |
| Tray applet configuration | `docs/Tray-Applets.md` | (tray extras) |

### Utility Modules

| User asks about... | Read this file | Module name |
|--------------------|----------------|-------------|
| Date and time | `docs/Module:-Clock.md` | `clock` |
| Custom scripts/output | `docs/Module:-Custom.md` | `custom/*` |
| Custom module examples | `docs/Module:-Custom:-Examples.md` | (examples) |
| Custom menus | `docs/Module:-Custom:-Menu.md` | (menus) |
| Third-party custom modules | `docs/Module:-Custom:-Third-party.md` | (third-party) |
| Grouping modules | `docs/Module:-Group.md` | `group/*` |
| Idle inhibitor | `docs/Module:-Idle-Inhibitor.md` | `idle_inhibitor` |
| GameMode status | `docs/Module:-Gamemode.md` | `gamemode` |
| Power profiles | `docs/Module:-PowerProfilesDaemon.md` | `power-profiles-daemon` |
| User info | `docs/Module:-User.md` | `user` |

### Development

| Topic | File |
|-------|------|
| Creating custom modules | `docs/Writing-Modules.md` |
| CFFI (foreign function) | `docs/Module:-CFFI.md` |
| Module states | `docs/States.md` |

## Keyword Quick Reference

Common search terms -> doc file:

- **volume, audio, sound** -> `Module:-PulseAudio.md` or `Module:-WirePlumber.md`
- **wifi, ethernet, internet** -> `Module:-Network.md`
- **time, date, clock format** -> `Module:-Clock.md`
- **colors, font, styling** -> `Styling.md`
- **icons, fonts, nerd fonts** -> `Styling.md` + `FAQ.md`
- **click actions, on-click** -> Individual module docs (most support it)
- **tooltip, hover** -> Individual module docs
- **format, format-icons** -> Individual module docs
- **workspaces, tags** -> Compositor-specific module docs
- **custom script, exec** -> `Module:-Custom.md`
- **slider, scroll** -> `Module:-PulseAudio-Slider.md`, `Module:-Backlight-Slider.md`
- **multiple bars, multi-monitor** -> `Configuration.md`
- **hide, autohide** -> `Configuration.md`
- **layers, exclusive zone** -> `Configuration.md`

## Config Structure Overview

```jsonc
// ~/.config/waybar/config.jsonc
{
    "layer": "top",          // top or bottom layer
    "position": "top",       // top, bottom, left, right
    "height": 30,            // bar height in pixels
    "modules-left": ["sway/workspaces", "sway/mode"],
    "modules-center": ["clock"],
    "modules-right": ["network", "battery", "tray"],

    // Module-specific configuration
    "clock": {
        "format": "{:%H:%M}",
        "tooltip-format": "{:%Y-%m-%d}"
    }
}
```

## Style Structure Overview

```css
/* ~/.config/waybar/style.css */
* {
    font-family: "JetBrains Mono", monospace;
    font-size: 14px;
}

window#waybar {
    background: rgba(0, 0, 0, 0.8);
    color: white;
}

#clock, #battery, #network {
    padding: 0 10px;
}
```
