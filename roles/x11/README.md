---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: desktop
role: x11
---

# `mps.desktop.x11`

Install X11 server, mesa, and qtile build dependencies

## Default variables

| Variable | Default | Description |
|---|---|---|
| `x11_packages` | `[11 items]` | List of apt packages to install for X11 stack |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.desktop.x11
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 3
