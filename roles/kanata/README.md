---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: desktop
role: kanata
---

# `mps.desktop.kanata`

Install kanata keyboard remapper + per-user systemd service

## Default variables

| Variable | Default | Description |
|---|---|---|
| `kanata_cargo_features` | `cmd` | Cargo features for kanata (e.g. 'cmd', 'passthru_ahk') |
| `kanata_config_path` | `~/.config/kanata/kanata.kbd` | Per-user kanata config path (use `~` for home dir) |
| `kanata_modules_load_content` | `uinput
` | Content of the modules-load config for uinput |
| `kanata_modules_load_path` | `/etc/modules-load.d/uinput.conf` | Path to install the modules-load config for uinput |
| `kanata_packages` | `- udev` | Apt packages required for kanata (uinput group, udev rules) |
| `kanata_udev_rule_content` | `KERNEL=="uinput", MODE="0660", GROUP="uinput", OPTIONS+="static_node=uinput"
` | Content of the udev rule for uinput |
| `kanata_udev_rule_path` | `/etc/udev/rules.d/99-kanata-uinput.rules` | Path to install the udev rule for uinput |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.desktop.kanata
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 176
