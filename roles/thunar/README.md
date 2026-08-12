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
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 8
