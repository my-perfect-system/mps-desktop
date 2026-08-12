---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: desktop
role: brave
---

# `mps.desktop.brave`

Install Brave browser via HTTPS APT repo

## Default variables

| Variable | Default | Description |
|---|---|---|
| `brave_apt_filename` | `brave-browser` | Filename for the Brave APT source list |
| `brave_keyring_path` | `/usr/share/keyrings/brave-browser-archive-keyring.gpg` | Path to the Brave GPG keyring |
| `brave_packages` | `- ca-certificates<br>- curl<br>- gnupg<br>- apt-transport-https` | APT packages required to install Brave (prereqs) |
| `brave_repo_url` | `https://brave-browser-apt-release.s3.brave.com/` | Base URL for Brave APT repository and key |

## Dependencies

None.

## Example usage

```yaml
- hosts: all
  roles:
    - mps.desktop.brave
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 3
