---
namespace: mps
collection: desktop
role: qtile
---

# `mps.desktop.qtile`

Install qtile + per-user templated Python config

## Default variables

| Variable | Default | Description |
|---|---|---|
| `qtile_autostart_displays` | `- mode: 3840x2160<br>  name: PRIMARY<br>  output: HDMI-1<br>  position: 0<br>  primary: true<br>  scale: 1.0x1.0<br>- mode: 1920x1080<br>  name: SECONDARY<br>  output: DP-1<br>  position: 3840x1080<br>  primary: false<br>  scale: 1.6x1.6` | Display list for xrandr in qtile-autostart-start.bash |
| `qtile_autostart_keyboard` | `de` | Keyboard layout for setxkbmap in qtile-autostart-start.bash |
| `qtile_autostart_xset_rate` | `xset r rate 250 50` | xset rate command for qtile-autostart-start.bash |
| `qtile_kanata_state_path` | `/tmp/kanata.state` | Path to the kanata state file (must match mps.desktop.kanata.kanata_state_path) |
| `qtile_local_bin_dir` | `/usr/local/bin` | System-wide bin dir for qtile scripts |
| `qtile_local_bin_scripts` | `- qtile-startup.bash<br>- qtile-reload.bash<br>- qtile-restart.bash` | Qtile scripts to deploy to /usr/local/bin/ |
| `qtile_packages` | `[9 items]` | Qtile apt dependencies |
| `qtile_repo_dest` | `~/venvs/qtile/src` | Per-user path to clone the qtile repo (use ~ for home dir) |
| `qtile_repo_url` | `https://github.com/qtile/qtile` | Git URL of the qtile repository |
| `qtile_repo_version` | `v0.31.0` | Git ref (tag/branch) of the qtile repository to clone |
| `qtile_scratchpad_dropdowns` | `[6 items]` | Scratchpad DropDown definitions for qtile-scratchpad.py |
| `qtile_user_scripts` | `- qtile-autostart-start.bash<br>- qtile-autostart-stop.bash` | Qtile scripts to deploy to ~/.local/bin/ (per-user) |
| `qtile_venv_path` | `~/.venvs/qtile` | Python venv path for qtile (defaults to ~/.venvs/qtile to avoid collision with mps.terminal.python) |
| `qtile_vpn_admin_host` | `bks-adm` | Hostname of the admin VPN connection (FortiClient widget) |
| `qtile_vpn_pub_host` | `pub-all` | Hostname of the public VPN connection (FortiClient widget) |
| `qtile_wallpapers` | `[]` | List of wallpaper filenames. If empty, falls back to essentials_wallpapers_list. Keys are mapped 1-0. |
| `qtile_wallpapers_dir` | `/usr/share/images/desktop/wallpaper` | Directory where wallpaper images are deployed (used for building qtile wallpaper dict) |
| `qtile_xsessions_dir` | `/usr/share/xsessions` | Xsession .desktop file directory |
| `qtile_xsessions_file` | `qtile.desktop` | Xsession .desktop file name |
| `qtile_xsessions_path` | `{{ qtile_xsessions_dir }}/{{ qtile_xsessions_file }}` | Full destination path for the xsession .desktop file (derived from dir+file) |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.desktop.qtile
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 8

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
