---
namespace: mps
collection: desktop
role: spotify
---

# `mps.desktop.spotify`

Install Spotify client via HTTPS APT repo

## Default variables

| Variable | Default | Description |
|---|---|---|
| `spotify_apt_filename` | `spotify` | Filename for the Spotify APT source list |
| `spotify_key_url` | `https://download.spotify.com/debian/pubkey_5384CE82BA52C83A.asc` | URL to download the Spotify public key |
| `spotify_keyring_path` | `/etc/apt/trusted.gpg.d/spotify.gpg` | Destination path for the dearmored Spotify GPG key |
| `spotify_packages` | `- ca-certificates<br>- curl<br>- gnupg<br>- apt-transport-https` | APT packages required to install Spotify (prereqs) |
| `spotify_repo_url` | `https://repository.spotify.com` | Base URL for the Spotify APT repository |

## Dependencies

None.

## Example usage

```yaml
- hosts: all
  roles:
    - mps.desktop.spotify
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
