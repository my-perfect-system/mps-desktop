---
namespace: odem
collection: desktop
role: lightdm
---

# `odem.desktop.lightdm`

Configure lightdm-gtk-greeter background

## Default variables

| Variable | Default | Description |
|---|---|---|
| `lightdm_greeter_conf` | `/etc/lightdm/lightdm-gtk-greeter.conf` | Path to the lightdm gtk greeter config file |
| `lightdm_wallpaper` | `wormhole.jpg` | Wallpaper filename (must be in lightdm_wallpapers_dir) |
| `lightdm_wallpapers_dir` | `/usr/share/images/desktop/wallpaper` | Directory containing wallpaper images (odem.desktop.essentials deploys this) |

## Dependencies

None.

## Example usage

```yaml
- hosts: all
  roles:
    - odem.desktop.lightdm
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
