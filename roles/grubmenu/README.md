---
namespace: odem
collection: desktop
role: grubmenu
---

# `odem.desktop.grubmenu`

Install GRUB boot menu themes

## Default variables

| Variable | Default | Description |
|---|---|---|
| `grubmenu_app_version` | `1.0` | Version string to substitute in theme.txt (replaces CFG_VERSION placeholder) |
| `grubmenu_default_theme` | `anon` | Default GRUB theme (must be a dir under grubmenu_themes_dir) |
| `grubmenu_gfxmode` | `1920x1080` | Value to set for GRUB_GFXMODE in /etc/default/grub |
| `grubmenu_icons` | `- light` | List of icon set directory names (relative to files/grub/icons/) to deploy |
| `grubmenu_icons_dir` | `/boot/grub/icons` | Destination directory for GRUB icons |
| `grubmenu_themes` | `- anon<br>- showroom` | List of theme directory names (relative to files/grub/themes/) to deploy |
| `grubmenu_themes_dir` | `/boot/grub/themes` | Destination directory for GRUB themes |

## Dependencies

None.

## Example usage

```yaml
- hosts: all
  roles:
    - odem.desktop.grubmenu
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 3

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
