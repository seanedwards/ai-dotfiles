---
name: using-bazzite
description: Use when helping with Bazzite Linux, installing software, configuring handhelds/Steam Deck, gaming setup, system updates/rollbacks, or troubleshooting Bazzite-specific issues - navigates comprehensive reference documentation
---

# Using Bazzite

Bazzite is a Fedora Atomic (immutable) Linux distribution optimized for gaming, with special editions for Steam Deck, handheld PCs, and HTPCs. This skill navigates the complete Bazzite documentation to answer usage and configuration questions.

**Key commands:** `ujust` (system tasks) | `rpm-ostree` (system packages) | `flatpak` (apps) | `distrobox` (containers)

**Update:** System updates automatically; manual: `ujust update`

## How to Use This Skill

1. Identify user intent from the topic index below
2. Read the relevant doc file(s) from the `docs/src/` subdirectory (paths are relative to this skill's directory)
3. Answer using the documentation content

**Always read docs before answering** - don't rely on general knowledge about Bazzite.

## Bazzite Image Variants

Users must choose the correct image. Key decision points:

| Question | Image Type |
|----------|------------|
| Desktop/laptop without Steam Gaming Mode? | `bazzite` or `bazzite-gnome` |
| Need Nvidia GPU support? | Add `-nvidia` (legacy) or `-nvidia-open` (RTX/GTX 16+) |
| Want Steam Gaming Mode (console-like)? | `bazzite-deck` variants |
| Software development focus? | Rebase to `bazzite-dx` |

**Check current image:** `rpm-ostree status`

For detailed image selection, read `docs/src/General/FAQ.md` (see "What Bazzite image do I use?")

## Topic Index

### Getting Started

| User asks about... | Read this file |
|--------------------|----------------|
| What is Bazzite, overview | `docs/src/index.md` |
| General section overview | `docs/src/General/index.md` |
| Common questions, which image to use | `docs/src/General/FAQ.md` |
| Terminology (immutable, ostree, etc) | `docs/src/General/terms.md` |
| Comparison to Fedora Atomic/Silverblue | `docs/src/General/Fedora_Atomic_Comparison.md` |
| Comparison to SteamOS | `docs/src/General/SteamOS_Comparison.md` |
| Community resources, external guides | `docs/src/General/community-links.md` |

### Installation Guides

| User asks about... | Read this file |
|--------------------|----------------|
| Installation overview | `docs/src/General/Installation_Guide/index.md` |
| Desktop/laptop install | `docs/src/General/Installation_Guide/Installing_Bazzite_for_Desktop_or_Laptop_Hardware.md` |
| Steam Deck install | `docs/src/General/Installation_Guide/Installing_Bazzite_for_Steam_Deck.md` |
| Handheld PC install | `docs/src/General/Installation_Guide/Installing_Bazzite_for_Handheld_PCs.md` |
| HTPC setup install | `docs/src/General/Installation_Guide/Installing_Bazzite_for_HTPC_Setups.md` |
| Framework 13 install | `docs/src/General/Installation_Guide/Installing_Bazzite_Framework_Laptop_13.md` |
| Framework 16 install | `docs/src/General/Installation_Guide/Installing_Bazzite_for_Framework_Laptop_16.md` |
| Dual boot setup | `docs/src/General/Installation_Guide/dual_boot_setup_guide.md` |
| Manual partitioning | `docs/src/General/Installation_Guide/manual_partitioning.md` |
| Secure boot | `docs/src/General/Installation_Guide/secure_boot.md` |
| Installation troubleshooting | `docs/src/General/Installation_Guide/troubleshoot_guide.md` |
| Alternate install methods | `docs/src/General/Installation_Guide/alternate-install-guide.md` |
| Uninstalling Bazzite | `docs/src/General/uninstalling-bazzite.md` |

### Installing Software

| User asks about... | Read this file |
|--------------------|----------------|
| Software install overview, priority | `docs/src/Installing_and_Managing_Software/index.md` |
| ujust commands, Bazzite Portal | `docs/src/Installing_and_Managing_Software/ujust.md` |
| Flatpak apps | `docs/src/Installing_and_Managing_Software/Flatpak.md` |
| Homebrew packages | `docs/src/Installing_and_Managing_Software/Homebrew.md` |
| Distrobox containers | `docs/src/Installing_and_Managing_Software/Distrobox.md` |
| Quadlet/Podman containers | `docs/src/Installing_and_Managing_Software/Quadlet.md` |
| AppImage apps | `docs/src/Installing_and_Managing_Software/AppImage.md` |
| rpm-ostree (discouraged) | `docs/src/Installing_and_Managing_Software/rpm-ostree.md` |
| Android apps (Waydroid) | `docs/src/Installing_and_Managing_Software/Waydroid_Setup_Guide.md` |

### Updates, Rollbacks & Rebasing

| User asks about... | Read this file |
|--------------------|----------------|
| Updates overview | `docs/src/Installing_and_Managing_Software/Updates_Rollbacks_and_Rebasing/index.md` |
| How to update | `docs/src/Installing_and_Managing_Software/Updates_Rollbacks_and_Rebasing/updating_guide.md` |
| Rolling back updates | `docs/src/Installing_and_Managing_Software/Updates_Rollbacks_and_Rebasing/rolling_back_system_updates.md` |
| Rollback helper tool | `docs/src/Installing_and_Managing_Software/Updates_Rollbacks_and_Rebasing/bazzite_rollback_helper.md` |
| Rebasing to different image | `docs/src/Installing_and_Managing_Software/Updates_Rollbacks_and_Rebasing/rebase_guide.md` |

### Gaming

| User asks about... | Read this file |
|--------------------|----------------|
| Gaming overview | `docs/src/Gaming/index.md` |
| Steam setup, Proton, launch options | `docs/src/Gaming/Game_Launchers.md` |
| Lutris, non-Steam games | `docs/src/Gaming/Game_Launchers.md` |
| Heroic, Epic, GOG, Amazon | `docs/src/Gaming/Game_Launchers.md` |
| Hardware compatibility (GPU, controllers) | `docs/src/Gaming/Hardware_compatibility_for_gaming.md` |
| Modding games (Nexus, Vortex, MO2) | `docs/src/Gaming/Managing_and_modding_games.md` |
| Common gaming issues | `docs/src/Gaming/Common_gaming_issues.md` |

### Handheld & HTPC Edition (Steam Gaming Mode)

| User asks about... | Read this file |
|--------------------|----------------|
| Steam Gaming Mode overview | `docs/src/Handheld_and_HTPC_edition/Steam_Gaming_Mode.md` |
| Handheld wiki overview | `docs/src/Handheld_and_HTPC_edition/Handheld_Wiki/index.md` |
| Steam Deck specifics | `docs/src/Handheld_and_HTPC_edition/Handheld_Wiki/Steam_Deck.md` |
| Lenovo Legion Go | `docs/src/Handheld_and_HTPC_edition/Handheld_Wiki/Lenovo_Legion_Go.md` |
| ASUS ROG Ally | `docs/src/Handheld_and_HTPC_edition/Handheld_Wiki/ASUS_ROG_Ally.md` |
| GPD handhelds | `docs/src/Handheld_and_HTPC_edition/Handheld_Wiki/GPD_Handhelds.md` |
| OneXPlayer | `docs/src/Handheld_and_HTPC_edition/Handheld_Wiki/OneXPlayer_Handhelds.md` |
| Ayaneo handhelds | `docs/src/Handheld_and_HTPC_edition/Handheld_Wiki/Ayaneo_Handhelds.md` |
| Ayn handhelds | `docs/src/Handheld_and_HTPC_edition/Handheld_Wiki/Ayn_Handhelds.md` |
| Other handhelds | `docs/src/Handheld_and_HTPC_edition/Handheld_Wiki/Other_Handhelds.md` |
| Gaming Mode quirks, workarounds | `docs/src/Handheld_and_HTPC_edition/quirks.md` |
| Legion Go BIOS update | `docs/src/Handheld_and_HTPC_edition/update-bios-lenovo-legion-go.md` |

### Troubleshooting & Configuration

| User asks about... | Read this file |
|--------------------|----------------|
| Common issues & fixes | `docs/src/General/issues_and_resolutions.md` |
| Reporting bugs | `docs/src/General/reporting_bugs.md` |
| KDE/GNOME customization, themes | `docs/src/General/Desktop_Environment_Tweaks.md` |
| VPN setup | `docs/src/General/VPN.md` |
| ZeroTier networking | `docs/src/General/zerotier.md` |

### Advanced Topics

| User asks about... | Read this file |
|--------------------|----------------|
| Advanced overview | `docs/src/Advanced/index.md` |
| Bazzite CLI tool | `docs/src/Advanced/bazzite-cli.md` |
| Auto-mounting drives | `docs/src/Advanced/Auto-Mounting_Secondary_Drives.md` |
| Custom resolutions | `docs/src/Advanced/custom_resolution.md` |
| Swap file configuration | `docs/src/Advanced/swapfile.md` |
| Reset forgotten password | `docs/src/Advanced/Reset_Forgotten_User_Password.md` |
| Rescue/emergency mode | `docs/src/Advanced/rescue-and-emergency-mode.md` |
| Dracut/initramfs | `docs/src/Advanced/dracut-and-initramfs.md` |
| Plymouth boot screen | `docs/src/Advanced/plymouth_init.md` |
| Shell best practices | `docs/src/Advanced/Best_Shell_Practices.md` |
| Creating custom images | `docs/src/Advanced/creating_custom_image.md` |
| Looking Glass (VM gaming) | `docs/src/Advanced/looking-glass.md` |
| SteelSeries Arctis manager | `docs/src/Advanced/arctis-manager.md` |
| ScopeBuddy (gamescope options) | `docs/src/Advanced/scopebuddy.md` |

## Keyword Quick Reference

Common search terms -> doc file (all paths under `docs/src/`):

### Installation & Setup
- **install, setup, ISO** -> `General/Installation_Guide/` (by device type)
- **dual boot, windows** -> `General/Installation_Guide/dual_boot_setup_guide.md`
- **secure boot, mokutil** -> `General/Installation_Guide/secure_boot.md`
- **partition, btrfs** -> `General/Installation_Guide/manual_partitioning.md`
- **which image, -deck, -gnome** -> `General/FAQ.md`

### Software Management
- **ujust, just, bazzite portal** -> `Installing_and_Managing_Software/ujust.md`
- **flatpak, flathub** -> `Installing_and_Managing_Software/Flatpak.md`
- **brew, homebrew** -> `Installing_and_Managing_Software/Homebrew.md`
- **container, distrobox, podman** -> `Installing_and_Managing_Software/Distrobox.md`
- **android, waydroid** -> `Installing_and_Managing_Software/Waydroid_Setup_Guide.md`
- **layer, rpm-ostree** -> `Installing_and_Managing_Software/rpm-ostree.md`

### Updates & System
- **update, upgrade** -> `Installing_and_Managing_Software/Updates_Rollbacks_and_Rebasing/updating_guide.md`
- **rollback, downgrade, revert** -> `Installing_and_Managing_Software/Updates_Rollbacks_and_Rebasing/rolling_back_system_updates.md`
- **rebase, switch image** -> `Installing_and_Managing_Software/Updates_Rollbacks_and_Rebasing/rebase_guide.md`
- **immutable, atomic, ostree** -> `General/terms.md` + `General/Fedora_Atomic_Comparison.md`

### Gaming
- **steam, proton, wine, launch options** -> `Gaming/Game_Launchers.md`
- **lutris, heroic, gog, epic** -> `Gaming/Game_Launchers.md`
- **nvidia, amd, gpu, driver** -> `Gaming/Hardware_compatibility_for_gaming.md`
- **controller, gamepad, joystick** -> `Gaming/Hardware_compatibility_for_gaming.md` + `General/issues_and_resolutions.md`
- **mod, nexus, vortex, mo2** -> `Gaming/Managing_and_modding_games.md`
- **dlss, fsr, upscaling** -> `Gaming/Game_Launchers.md`

### Handheld/HTPC
- **deck, gaming mode, gamescope** -> `Handheld_and_HTPC_edition/Steam_Gaming_Mode.md`
- **legion go, rog ally** -> Device-specific in `Handheld_and_HTPC_edition/Handheld_Wiki/`
- **decky, css loader** -> `General/Desktop_Environment_Tweaks.md`
- **big picture, couch** -> `Handheld_and_HTPC_edition/Steam_Gaming_Mode.md`

### Troubleshooting
- **wifi, ethernet, network** -> `General/issues_and_resolutions.md`
- **audio, sound, volume** -> `General/issues_and_resolutions.md`
- **auto login** -> `General/issues_and_resolutions.md`
- **fast startup (Windows)** -> `General/issues_and_resolutions.md`
- **kde, gnome, theme** -> `General/Desktop_Environment_Tweaks.md`

## Software Installation Priority

Bazzite recommends software installation methods in this order:

1. **ujust** - System tasks and curated software (`ujust --choose`)
2. **Flatpak** - Sandboxed desktop apps (Flathub)
3. **Homebrew** - CLI tools and development packages
4. **Quadlet** - Containerized services (Podman)
5. **Distrobox** - Full Linux environments in containers
6. **AppImage** - Portable standalone apps
7. **rpm-ostree** - Layer system packages (discouraged, use sparingly)

## Key Commands Reference

```bash
# System updates
ujust update              # Update everything
ujust bios                # Check BIOS updates (Framework, handhelds)

# Software discovery
ujust                     # List all available commands
ujust --choose            # Interactive menu of available tasks
ujust | grep "keyword"    # Search for specific commands

# View ujust script source
ujust --show <command>    # See what a command does before running

# Rollback
ujust rollback            # Rollback helper
rpm-ostree rollback       # Manual rollback to previous deployment

# Rebase (switch images)
rpm-ostree rebase ostree-image-signed:docker://ghcr.io/ublue-os/bazzite:stable

# System info
rpm-ostree status         # Show current and previous deployments
```

## ujust Command Prefixes

| Prefix | Purpose | Example |
|--------|---------|---------|
| `install-` | Install software | `ujust install-decky` |
| `setup-` | Install with config/uninstall options | `ujust setup-gaming` |
| `configure-` | Configure existing features | `ujust configure-waydroid` |
| `toggle-` | Enable/disable features | `ujust toggle-updates` |
| `fix-` | Fix/patch issues | `ujust fix-audio` |
| `get-` | Get extensions/plugins | `ujust get-decky-plugins` |
| (no prefix) | Common shortcuts | `ujust update`, `ujust rollback` |
