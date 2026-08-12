---
namespace: odem
collection: desktop
role: gnometools
---

# `odem.desktop.gnometools`

Install GNOME desktop tools

## Dependencies

None.

## Example usage

```yaml
- hosts: all
  roles:
    - odem.desktop.gnometools
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
