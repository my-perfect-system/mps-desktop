---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: desktop
role: lightdm
---

# `mps.desktop.lightdm`

Configure lightdm-gtk-greeter background

## Default variables

| Variable | Default | Description |
|---|---|---|
| `lightdm_greeter_conf` | `/etc/lightdm/lightdm-gtk-greeter.conf` | Path to the lightdm gtk greeter config file |
| `lightdm_wallpaper` | `wormhole.jpg` | Wallpaper filename (must be in lightdm_wallpapers_dir) |
| `lightdm_wallpapers_dir` | `/usr/share/images/desktop/wallpaper` | Directory containing wallpaper images (mps.desktop.essentials deploys this) |

## Dependencies

None.

## Example usage

```yaml
- hosts: all
  roles:
    - mps.desktop.lightdm
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 3
