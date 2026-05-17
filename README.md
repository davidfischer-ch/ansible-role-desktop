# Ansible Role Desktop

Library of Ansible plugins and roles for deploying various services.
See [ansible-roles](https://github.com/davidfischer-ch/ansible-roles) for additional documentation.

This repository hosts the role Desktop and may depend of other roles and plugins of the library.

## Dependencies

See [meta](meta/main.yml).

## Variables

| Variable | Default | Description |
|---|---|---|
| `desktop_snap_mode` | `enabled` | Snap management mode: `enabled` (keep snap), `partial` (remove managed packages, keep snap daemon), `disabled` (purge snap entirely). |
| `desktop_snap_flush_packages` | `{{ web_packages }}` | Snap package names to remove in `partial` and `disabled` modes. Names must match snap identifiers (may differ from apt names, e.g. `chromium` not `chromium-browser`). Failures are silenced. |
| `desktop_snap_directories` | `/snap`, `/var/snap`, `/var/lib/snapd`, `/var/cache/snapd` | Directories to purge in `disabled` mode. |

## License

See [LICENSE.rst](LICENSE.rst).

## Authors

See [AUTHORS](AUTHORS).

2014-2022 - David Fischer
