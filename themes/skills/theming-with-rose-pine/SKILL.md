---
name: theming-with-rose-pine
description: Use when the user wants to theme an application with Rose Pine colors - navigates Rose Pine documentation to find app-specific configuration and guides the user through installation
---

# Theming with Rose Pine

## Overview

Rose Pine is a cohesive color theme with 207+ application ports. Each application has unique installation instructions. This skill navigates the Rose Pine ecosystem to find and apply the correct configuration.

## Rose Pine Variants

Always present all three options to the user:

| Variant | Description | Best For |
|---------|-------------|----------|
| **Rose Pine** (main) | Balanced, warm tones | General use |
| **Rose Pine Moon** | Darkest, cooler tones | Low-light, high contrast |
| **Rose Pine Dawn** | Lightest, warm undertones | Bright environments |

## Finding Theme Configuration

**Search priority:**

1. **rosepinetheme.com/themes/** - Primary source with 207 ports
   - Use WebFetch to search/browse the themes page
   - Categories: app, CLI, editor, terminal, shell, mobile, music

2. **github.com/rose-pine/[app-name]** - Official repositories
   - Direct pattern: `github.com/rose-pine/neovim`, `github.com/rose-pine/kitty`, etc.
   - Use WebFetch or `gh` CLI to access README

3. **Community contributions** - Linked from main site
   - May be under different GitHub organizations
   - Quality varies; prefer official ports

## Workflow

### Step 1: Identify the Application

Ask the user which application they want to theme if not specified. Common categories:
- **Terminal emulators**: kitty, alacritty, wezterm, foot, ghostty
- **Editors**: neovim, vim, vscode, emacs, helix
- **Shells**: fish, zsh, bash
- **Desktop**: gtk, kde, qt
- **Apps**: discord, spotify, firefox, obsidian

### Step 2: Find the Theme

```
WebFetch: https://rosepinetheme.com/themes/
Prompt: "Find the Rose Pine theme for [application]. Return the GitHub repository URL and any installation instructions visible."
```

If not found on the themes page:
```
WebFetch: https://github.com/rose-pine/[app-name]
Prompt: "Extract the installation instructions from this Rose Pine theme README."
```

### Step 3: Present Options to User

Before applying, confirm:
1. Which variant? (main, moon, dawn)
2. Installation method (if multiple options)
3. Configuration file location (verify it exists)

### Step 4: Apply Configuration

Each application is different. Common patterns:

**Config file themes** (kitty, alacritty, foot):
- Download/copy theme file to config directory
- Add `include` or `import` statement to main config

**Plugin-based** (neovim, vim, emacs):
- Add plugin to package manager
- Configure colorscheme in config file

**Manual installation** (discord, spotify):
- May require custom clients (BetterDiscord, Spicetify)
- Follow app-specific instructions exactly

### Step 5: Verify

- Restart the application or reload configuration
- Confirm colors applied correctly
- Offer to switch variants if user wants to compare

## Example Interactions

**User:** "Theme kitty with rose pine"

1. WebFetch rosepinetheme.com/themes/ to find kitty
2. Find: github.com/rose-pine/kitty
3. Ask: "Which variant: main, moon, or dawn?"
4. Locate kitty config: `~/.config/kitty/kitty.conf`
5. Download theme file from GitHub
6. Add include statement to kitty.conf
7. Instruct user to restart kitty

**User:** "I want rose pine in neovim"

1. WebFetch github.com/rose-pine/neovim
2. Identify plugin manager (lazy.nvim, packer, vim-plug)
3. Ask: "Which variant? And which plugin manager are you using?"
4. Provide plugin configuration snippet
5. Add colorscheme command to init.lua/init.vim

## Key Resources

| Resource | URL | Use For |
|----------|-----|---------|
| Theme directory | rosepinetheme.com/themes/ | Finding any app's theme |
| Palette reference | rosepinetheme.com/palette/ | Understanding color values |
| GitHub org | github.com/rose-pine | Official theme repos |
| Contribution guide | rosepinetheme.com/resources/create-a-theme/ | Creating new ports |

## Common Issues

| Problem | Solution |
|---------|----------|
| Theme not found | Check spelling, search community contributions |
| Colors look wrong | Verify terminal supports true color (24-bit) |
| Partial theming | Some apps need multiple configs (GTK + Qt, editor + terminal) |
| Changes not applying | Restart app, check config file syntax |

## Do NOT

- Copy entire theme configs into responses (they change over time)
- Assume installation steps without checking the README
- Skip asking about variant preference
- Forget to verify the user's config file location exists
