# APT 

[![Build Status](https://travis-ci.org/rroethof/ansible-apt.svg?branch=master)](https://travis-ci.org/rroethof/ansible-apt)

Ansible role for execute apt-get update and install apt-repositories and apt-packages.


## Requirements

None


## Role Variables

See [defaults/main.yml](defaults/main.yml) for more information.

```yaml
    apt_cache_valid_time: 3600
    apt_upgrade: true
    apt_upgrade_type: safe          # safe, full or dist
    apt_install:
      - python-apt
      - unattended-upgrades
    apt_install_repositories: false
    apt_remove_repositories: false
```


## Dependencies


## Examples

```yaml
    - hosts: localhost
      vars:
          apt_install: [sl, figlet]
      roles:
        - { role: apt, tags: apt }
```


## License


## Author Information

This role was created in 2015 by Ronny Roethof, based uppon [ansible-role-apt](https://github.com/kosssi/ansible-role-apt) by Simon Constans.