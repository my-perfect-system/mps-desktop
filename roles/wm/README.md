---
namespace: odem
collection: desktop
role: wm
---

# `odem.desktop.wm`

Install window manager deps and per-user dotfiles

## Default variables

| Variable | Default | Description |
|---|---|---|
| `wm_dotfiles` | `- .config/picom.conf<br>- .config/dunst` | Per-user dotfile paths to copy (dconf config is owned by odem.desktop.essentials) |
| `wm_packages` | `[23 items]` | Window manager packages |

## Dependencies

- `odem.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - odem.desktop.wm
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
