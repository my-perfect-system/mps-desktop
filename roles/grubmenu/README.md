---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: desktop
role: grubmenu
---

# `mps.desktop.grubmenu`

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
    - mps.desktop.grubmenu
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 3
