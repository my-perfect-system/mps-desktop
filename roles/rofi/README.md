---
namespace: mps
collection: desktop
role: rofi
---

# `mps.desktop.rofi`

Install rofi launcher + per-user config and 8 boot scripts

## Default variables

| Variable | Default | Description |
|---|---|---|
| `rofi_dotfiles` | `- .config/rofi` | Per-user rofi dotfile path |
| `rofi_packages` | `- rofi` | Rofi packages |
| `rofi_scripts` | `[8 items]` | Per-user rofi boot scripts to deploy to ~/.local/bin/ |
| `rofi_themes` | `- rofi-boot-autorandr.rasi<br>- rofi-boot-dwmswitch.rasi<br>- rofi-boot-launcher.rasi<br>- rofi-boot-powermenu.rasi` | Rofi theme filenames to deploy to rofi_themes_dir |
| `rofi_themes_dir` | `/usr/share/rofi/themes` | System-wide rofi themes directory |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.desktop.rofi
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
