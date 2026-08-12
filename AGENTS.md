# AGENTS.md — mps-desktop

Desktop GUI and window manager environment — x11, qtile window manager,
rofi / thunar / essentials helpers, kanata keyboard remapper, firefox /
thunderbird / brave / spotify browsers, lightdm greeter, plymouth boot
theme, gnome-tools.

## Galaxy

- **namespace**: `mps`
- **name**: `desktop`
- **version**: `0.3.1`
- **dependencies**: `mps.base >=0.1.0`, `ansible.posix >=1.0.0`

## Roles

### Browser / system apps (single-package installs)

| Role | Description | Complexity |
|---|---|---|
| `mps.desktop.firefox` | Firefox apt install. | 1 |
| `mps.desktop.thunderbird` | Thunderbird apt install. | 1 |
| `mps.desktop.brave` | Brave browser (custom apt repo + signing key). | 1 |
| `mps.desktop.spotify` | Spotify client (custom apt repo + signing key). | 1 |
| `mps.desktop.lightdm` | LightDM greeter config + wallpaper directory. | 1 |
| `mps.desktop.plymouth` | Plymouth boot theme + `.plymouth` file modification. | 1 |
| `mps.desktop.grubmenu` | GRUB theme + `/etc/default/grub` lineinfile + `update-grub`. | 1 |
| `mps.desktop.gnometools` | GNOME tool packages (single install list). | 1 |
| `mps.desktop.x11` | X11 base packages. | 1 |

### Window manager + helpers (per-user)

| Role | Description | Complexity |
|---|---|---|
| `mps.desktop.qtile` | 21 jinja2 templates (some with loops), heavy `set_fact` chains for per-user config paths, pip venv + git clone. **Most complex desktop role.** | 3 |
| `mps.desktop.kanata` | Per-user rustup / cargo install, udev rules, systemd user service, `enable-linger` loop. | 3 |
| `mps.desktop.essentials` | Per-user dotfile copy loops + per-user `set_fact` builders. | 2 |
| `mps.desktop.rofi` | Per-user dotfile + script copy loops + `set_fact` builders. | 2 |
| `mps.desktop.thunar` | Per-user dotfile copy loop + `set_fact`. | 2 |
| `mps.desktop.wm` | Per-user copy loops with `item.src` gating + `set_fact`. | 2 |

## Conventions

- Browser / system app roles are single-package installs (apt + optional GPG key); kept as `install.yml` + `main.yml` 2-file roles.
- WM + helper roles are per-user; each has `facts.yml` (set_fact builders) + `install.yml` (system packages) + `configure.yml` (per-user copy loops). Multi-file by design.
- Per-user loops use `block:` with `loop: "{{ identity_users_resolved | mps_filter_users('desktop_<x>') }}"`.
