---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
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
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 8
