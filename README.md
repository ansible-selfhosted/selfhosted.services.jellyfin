[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-inverted-border.json)](https://github.com/copier-org/copier)
[![Podman Badge](https://img.shields.io/badge/Podman-892CA0?logo=podman&logoColor=white)](https://podman.io/)
[![Hatch project](https://img.shields.io/badge/%F0%9F%A5%9A-Hatch-4051b5.svg)](https://github.com/pypa/hatch)
![CI](https://github.com/ansible-selfhosted/selfhosted.services.jellyfin/actions/workflows/ci.yml/badge.svg)
[![Ansible](https://img.shields.io/badge/Ansible-Molecule-EE0000?style=plastic&logo=ansible&logoColor=white)](https://github.com/ansible/molecule)

<!-- BEGIN_ANSIBLE_DOCS -->

# Ansible Role: [jellyfin](https://jellyfin.org/docs/)

A role to deploy Jellyfin using rootless Podman with systemd.

## Role Requirements

- none

*Refer to services collection for general requirements*

## Role Arguments

|Option|Description|Type|Required|Default|
|---|---|---|---|---|
|jellyfin_cache_path|The path for the Jellyfin cache.|str|False|~/.config/jellyfin/cache|
|jellyfin_config_path|The path for the Jellyfin config.|str|False|~/.config/jellyfin/config|
|jellyfin_hardware_encoding|If hardware encoding should be used.|bool|False|False|
|jellyfin_media_path|The path for the Jellyfin media.<br>It is recommended to share the same data directory with other media managing services|str|False|~/.local/share/containers/storage/media|
|jellyfin_version|The version of Jellyfin to install.|str|False|latest|
|jellyfin_web_port|The port for the web server.|int|False|8096|


## Example Playbook

```
- hosts: all
  tasks:
    - name: Importing jellyfin role
      ansible.builtin.import_role:
        name: selfhosted.services.jellyfin
      vars:
```

## License

This project is licensed under the [MIT License](LICENSE)


⊂(▀¯▀⊂)

<!-- END_ANSIBLE_DOCS -->
