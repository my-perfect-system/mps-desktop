---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: desktop
role: wm
---

# `mps.desktop.wm`

Install window manager deps and per-user dotfiles

## Default variables

| Variable | Default | Description |
|---|---|---|
| `wm_dotfiles` | `- .config/picom.conf<br>- .config/dunst` | Per-user dotfile paths to copy (dconf config is owned by mps.desktop.essentials) |
| `wm_packages` | `[23 items]` | Window manager packages |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.desktop.wm
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 8
