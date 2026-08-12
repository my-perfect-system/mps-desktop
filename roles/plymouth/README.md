---
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
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 3

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
