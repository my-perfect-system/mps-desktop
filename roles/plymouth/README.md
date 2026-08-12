---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: desktop
role: plymouth
---

# `mps.desktop.plymouth`

Install Plymouth boot splash theme

## Default variables

| Variable | Default | Description |
|---|---|---|
| `plymouth_default_theme` | `anon` | Custom Plymouth theme name (also used as GRUB theme name; should match grubmenu.grubmenu_default_theme) |
| `plymouth_packages` | `- plymouth<br>- plymouth-themes` | Apt packages required for Plymouth |
| `plymouth_themes_dir` | `/usr/share/plymouth/themes` | System Plymouth themes directory |

## Dependencies

None.

## Example usage

```yaml
- hosts: all
  roles:
    - mps.desktop.plymouth
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 3
