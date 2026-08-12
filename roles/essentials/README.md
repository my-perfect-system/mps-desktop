---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: desktop
role: essentials
---

# `mps.desktop.essentials`

Install desktop essentials and per-user GTK/gedit/dconf dotfiles

## Default variables

| Variable | Default | Description |
|---|---|---|
| `essentials_bootsplash_dst` | `/usr/share/images/desktop/bootsplash.png` | Destination path for the bootsplash image |
| `essentials_bootsplash_src` | `bootsplash.png` | Bootsplash image filename (relative to files/dotfiles/images/) |
| `essentials_dotfiles_dconf` | `- .config/dconf` | dconf config to copy per-user |
| `essentials_dotfiles_gedit` | `- .config/gedit` | gedit config to copy per-user |
| `essentials_dotfiles_gtk` | `- .gtkrc-2.0<br>- .config/gtk-2.0<br>- .config/gtk-3.0` | GTK2/GTK3 dotfiles to copy per-user |
| `essentials_packages_base` | `[11 items]` | Base desktop packages |
| `essentials_packages_sound` | `[5 items]` | Sound stack packages |
| `essentials_packages_xdg` | `- xdg-utils<br>- xdg-user-dirs` | XDG utilities packages |
| `essentials_wallpapers_dir` | `/usr/share/images/desktop/wallpaper` | Destination directory for wallpaper images |
| `essentials_wallpapers_list` | `[10 items]` | List of wallpaper filenames to deploy (from files/dotfiles/wallpaper/) |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.desktop.essentials
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
