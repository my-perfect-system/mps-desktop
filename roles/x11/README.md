---
namespace: odem
collection: desktop
role: x11
---

# `odem.desktop.x11`

Install X11 server, mesa, and qtile build dependencies

## Default variables

| Variable | Default | Description |
|---|---|---|
| `x11_packages` | `[11 items]` | List of apt packages to install for X11 stack |

## Dependencies

- `odem.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - odem.desktop.x11
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
