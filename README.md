Role Name
=========

An Ansible Role that installs [Jellyfin](https://jellyfin.org/) on Linux.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

    jellyfin_apt_gpg_key: https://repo.jellyfin.org/jellyfin_team.gpg.key

The location of the jellyfin apt key (usally an url).

    jellyfin_apt_arch: "{{ 'arm64' if ansible_architecture == 'aarch64' else 'armhf' if ansible_architecture == 'armv7l' else 'amd64' }}"

Architecture used for the Jellyfin repository.

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: tomhesse.jellyfin
```

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2024 by [tomhesse](https://www.tomhesse.xyz/).
