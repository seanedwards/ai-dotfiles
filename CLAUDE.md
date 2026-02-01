# ai-dotfiles

A Claude Code marketplace for personal plugins related to system administration and dotfile management on Bazzite Linux.

## Using This Marketplace

### Add the marketplace

```bash
/plugin marketplace add file:///var/home/edwards/Projects/ai-dotfiles
```

Or if you've cloned this repository elsewhere:
```bash
/plugin marketplace add file:///path/to/ai-dotfiles
```

### Browse available plugins

```bash
/plugin browse
```

### Install a plugin

```bash
/plugin install niri@ai-dotfiles
```

## Available Plugins

| Plugin | Description |
|--------|-------------|
| `niri` | Niri window manager configuration assistance |
| `themes` | Theme applications with Rose Pine color scheme |
| `waybar` | Waybar status bar configuration assistance |

## Adding New Plugins

1. Create plugin directory: `my-plugin/`
2. Add `.claude-plugin/plugin.json` with at minimum `{"name": "my-plugin"}`
3. Add components (commands, agents, skills, hooks)
4. Update `.claude-plugin/marketplace.json` to include the new plugin entry
5. Test: `/plugin reload` then `/plugin browse`
