# Omarchy Sapphire Theme - Complete Setup

This repository contains my complete Omarchy desktop environment configuration using the Sapphire theme. It includes everything from Hyprland window manager configuration to terminal emulator theming, waybar styling, and more.

## About Sapphire Theme

Inspired by the deep, timeless brilliance of sapphire gemstones — the rich blue base evokes clarity and depth, while touches of green, yellow and red bring life, precision and energy. This palette is chosen to reflect both calm concentration (blue) and subtle vitality (the accent colours), striking a balance between immersion and alertness. Crafted for a workspace that looks poised yet dynamic — where focus doesn't feel sterile, but alive with possibility.

## Screenshots
<img width="2560" height="1440" alt="screenshot-2025-10-23_06-27-38" src="https://github.com/user-attachments/assets/90cd0a7a-4f4f-4bfa-b015-6ec4752f362c" />
<img width="2560" height="1440" alt="screenshot-2025-11-02_00-30-17" src="https://github.com/user-attachments/assets/e3fe7ebc-51f7-4036-82e3-a6e4dd8416a5" />

## What's Included

This repository contains configurations for:

### Theme Files (Root Directory)
- **alacritty.toml** - Alacritty terminal theme
- **kitty.conf** - Kitty terminal theme
- **hyprland.conf** - Hyprland compositor theme settings
- **hyprlock.conf** - Hyprlock screen lock theme
- **waybar.css** - Waybar styling
- **gtk.css** - GTK application theming
- **mako.ini** - Notification daemon configuration
- **walker.css** - Walker application launcher theme
- **swayosd.css** - SwayOSD theme
- **btop.theme** - Btop system monitor theme
- **neovim.lua** - Neovim color scheme
- **ghostty.conf** - Ghostty terminal theme
- **vscode.json** - VS Code theme settings
- **chromium.theme** - Chromium browser theme
- **system24-Sapphire.css** - Vesktop/Discord theme
- **backgrounds/** - Wallpaper images
- **icons.theme** - Icon theme configuration

### Main Configuration Files (configs/ directory)

#### Hyprland (`configs/hypr/`)
Complete Hyprland configuration including:
- `hyprland.conf` - Main configuration
- `bindings.conf` - Keybindings
- `looknfeel.conf` - Appearance settings
- `input.conf` - Input device configuration
- `monitors.conf` - Monitor setup
- `autostart.conf` - Startup applications
- `envs.conf` - Environment variables
- `hypridle.conf` - Idle management
- `hyprsunset.conf` - Screen warming

#### Waybar (`configs/waybar/`)
- `config.jsonc` - Waybar module configuration
- `style.css` - Waybar styling

#### Terminal Emulators
- `configs/alacritty/alacritty.toml` - Alacritty main configuration
- `configs/kitty/kitty.conf` - Kitty main configuration

### Omarchy Files (`omarchy-files/`)
- `omarchy.ttf` - Omarchy custom font
- `hooks/theme-set` - Theme switching hook for pywal integration

## Dependencies

This setup requires the following packages:

- [Omarchy](https://omarchy.com) - Desktop environment manager
- Hyprland - Wayland compositor
- Waybar - Status bar
- Alacritty or Kitty - Terminal emulator
- Mako - Notification daemon
- Walker - Application launcher (optional)
- SwayOSD - On-screen display (optional)
- Btop - System monitor (optional)
- Pywal - For dynamic color generation (optional, used in theme-set hook)

## Installation

### Install the Sapphire Theme

To install just the Sapphire theme through Omarchy:

```bash
omarchy-theme-install https://github.com/HANCORE-linux/omarchy-sapphire-theme.git
```

### Full Configuration Setup

To replicate my complete setup:

1. **Clone this repository**:
   ```bash
   git clone https://github.com/YOUR-USERNAME/omarchy-sapphire-theme.git
   cd omarchy-sapphire-theme
   ```

2. **Install the theme files** (if using Omarchy):
   ```bash
   # The theme files in the root directory can be installed via omarchy-theme-install
   # or manually copied to ~/.config/omarchy/themes/sapphire/
   ```

3. **Copy main configuration files**:
   ```bash
   # Hyprland
   cp -r configs/hypr/* ~/.config/hypr/

   # Waybar
   cp configs/waybar/* ~/.config/waybar/

   # Alacritty
   cp configs/alacritty/alacritty.toml ~/.config/alacritty/

   # Kitty
   cp configs/kitty/kitty.conf ~/.config/kitty/
   ```

4. **Install Omarchy files**:
   ```bash
   # Font
   cp omarchy-files/omarchy.ttf ~/.config/

   # Hooks
   cp omarchy-files/hooks/theme-set ~/.config/omarchy/hooks/
   chmod +x ~/.config/omarchy/hooks/theme-set
   ```

5. **Set the theme** (if using Omarchy):
   ```bash
   omarchy-theme-set sapphire
   ```

6. **Reload your environment**:
   ```bash
   hyprctl reload
   ```

## Application-Specific Themes

### Vesktop/Discord Theme
Install the Discord theme:
```bash
cp system24-Sapphire.css ~/.config/vesktop/themes/system24-Sapphire.css
```

### Neovim Theme
This setup uses the [Pixel Theme](https://github.com/bjarneo/pixel.nvim) which adapts colors from terminal syntax.
- Check: https://github.com/bjarneo/pixel.nvim
- Make sure Lazyvim is up to date: `:Lazy`

### VSCode Theme
- Theme: Sapphire Theme
- Extension ID: `Tyriar.theme-sapphire`
- Install manually: Open VSCode > Extensions > Search "Sapphire Theme"

## Customization

The main configuration files in `configs/` reference the theme files through Omarchy's current theme symlink (`~/.config/omarchy/current/theme/`). This allows you to:

1. Switch themes easily through Omarchy
2. Keep your personal preferences (keybindings, monitor setup, etc.) separate from theme styling
3. Update theme colors without modifying main configs

## Structure

```
omarchy-sapphire-theme/
├── README.md                    # This file
├── LICENSE                      # MIT License
├── preview.png                  # Theme preview
├── backgrounds/                 # Wallpapers
├── configs/                     # Main configuration files
│   ├── hypr/                   # Hyprland configs
│   ├── waybar/                 # Waybar configs
│   ├── alacritty/              # Alacritty config
│   └── kitty/                  # Kitty config
├── omarchy-files/              # Omarchy-specific files
│   ├── omarchy.ttf             # Custom font
│   └── hooks/                  # Theme hooks
└── [theme files]               # All theme styling files
```

## Credits

- Original Sapphire theme by [HANCORE-linux](https://github.com/HANCORE-linux/omarchy-sapphire-theme)
- Omarchy desktop environment by the Omarchy team

## License

MIT

---

**Note**: This is my personal configuration. You may need to adjust paths, monitor settings, and keybindings to match your setup.
