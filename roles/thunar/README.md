---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: desktop
role: thunar
---

# `mps.desktop.thunar`

Install thunar + plugins and per-user dotfiles

## Default variables

| Variable | Default | Description |
|---|---|---|
| `thunar_dotfiles` | `- .config/Thunar<br>- .config/xfce4` | Per-user dotfile paths to copy |
| `thunar_packages` | `[6 items]` | Thunar core + plugin packages |
| `thunar_xfce_packages` | `- xfce4-goodies<br>- xfce4-places-plugin<br>- thunar-font-manager` | XFCE4 packages used by thunar |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.desktop.thunar
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
