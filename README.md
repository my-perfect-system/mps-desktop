# `mps.desktop` Ansible Collection

Desktop GUI and window manager environment — x11, qtile (WM), rofi /
thunar / essentials helpers, kanata keyboard remapper, firefox /
thunderbird / brave / spotify browsers, lightdm greeter, plymouth boot
theme, gnome-tools.

## Galaxy metadata

- **namespace**: `mps`
- **name**: `desktop`
- **version**: `0.3.1`
- **dependencies**: `mps.base`, `ansible.posix`

See [`galaxy.yml`](galaxy.yml) for the canonical values.

## Roles

### Browser / system apps

| Role | Purpose |
|---|---|
| `mps.desktop.firefox` | Firefox apt install. |
| `mps.desktop.thunderbird` | Thunderbird apt install. |
| `mps.desktop.brave` | Brave browser (apt repo + signing key). |
| `mps.desktop.spotify` | Spotify client (apt repo + signing key). |
| `mps.desktop.lightdm` | LightDM greeter config + wallpaper directory. |
| `mps.desktop.plymouth` | Plymouth boot theme. |
| `mps.desktop.grubmenu` | GRUB theme + `/etc/default/grub` + `update-grub`. |
| `mps.desktop.gnometools` | GNOME tool packages. |
| `mps.desktop.x11` | X11 base packages. |

### Window manager + helpers (per-user)

| Role | Purpose |
|---|---|
| `mps.desktop.qtile` | Templated qtile config, pip venv + git clone, per-user wallpaper dict. |
| `mps.desktop.kanata` | Per-user rustup install, udev rules, systemd user service. |
| `mps.desktop.essentials` | Per-user dotfile copies + facts builders. |
| `mps.desktop.rofi` | Per-user dotfile + script copies + facts builders. |
| `mps.desktop.thunar` | Per-user dotfile copies + facts. |
| `mps.desktop.wm` | Per-user copy loops (gated by `item.src`) + facts. |

## Installation

```bash
ansible-galaxy collection install mps.desktop
```

## Usage

```yaml
- hosts: desktops
  become: true
  vars:
    users_catalog:
      alice:
        user_roles:
          desktop_qtile: true
          desktop_kanata: true
  roles:
    - mps.base.identity
    - mps.desktop.x11
    - mps.desktop.qtile
```

## Documentation

- [`AGENTS.md`](AGENTS.md) — developer conventions
- `roles/<role>/README.md` — per-role variable docs

## License

GPL-3.0-or-later
