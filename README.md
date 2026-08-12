# `odem.desktop` Ansible Collection

Desktop GUI and window manager environment — x11, qtile (WM), rofi /
thunar / essentials helpers, kanata keyboard remapper, firefox /
thunderbird / brave / spotify browsers, lightdm greeter, plymouth boot
theme, gnome-tools.

## Galaxy metadata

- **namespace**: `odem`
- **name**: `desktop`
- **version**: `0.3.1`
- **dependencies**: `odem.base`, `ansible.posix`

See [`galaxy.yml`](galaxy.yml) for the canonical values.

## Roles

### Browser / system apps

| Role | Purpose |
|---|---|
| [`odem.desktop.firefox`](roles/firefox/README.md) | Firefox apt install. |
| [`odem.desktop.thunderbird`](roles/thunderbird/README.md) | Thunderbird apt install. |
| [`odem.desktop.brave`](roles/brave/README.md) | Brave browser (apt repo + signing key). |
| [`odem.desktop.spotify`](roles/spotify/README.md) | Spotify client (apt repo + signing key). |
| [`odem.desktop.lightdm`](roles/lightdm/README.md) | LightDM greeter config + wallpaper directory. |
| [`odem.desktop.plymouth`](roles/plymouth/README.md) | Plymouth boot theme. |
| [`odem.desktop.grubmenu`](roles/grubmenu/README.md) | GRUB theme + `/etc/default/grub` + `update-grub`. |
| [`odem.desktop.gnometools`](roles/gnometools/README.md) | GNOME tool packages. |
| [`odem.desktop.x11`](roles/x11/README.md) | X11 base packages. |

### Window manager + helpers (per-user)

| Role | Purpose |
|---|---|
| [`odem.desktop.qtile`](roles/qtile/README.md) | Templated qtile config, pip venv + git clone, per-user wallpaper dict. |
| [`odem.desktop.kanata`](roles/kanata/README.md) | Per-user rustup install, udev rules, systemd user service. |
| [`odem.desktop.essentials`](roles/essentials/README.md) | Per-user dotfile copies + facts builders. |
| [`odem.desktop.rofi`](roles/rofi/README.md) | Per-user dotfile + script copies + facts builders. |
| [`odem.desktop.thunar`](roles/thunar/README.md) | Per-user dotfile copies + facts. |
| [`odem.desktop.wm`](roles/wm/README.md) | Per-user copy loops (gated by `item.src`) + facts. |

## Installation

```bash
ansible-galaxy collection install odem.desktop
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
    - odem.base.identity
    - odem.desktop.x11
    - odem.desktop.qtile
```

## Documentation

- [`AGENTS.md`](AGENTS.md) — developer conventions
- `roles/<role>/README.md` — per-role variable docs

## License

GPL-3.0-or-later
