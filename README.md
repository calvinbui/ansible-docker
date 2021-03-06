[![Build Status](https://travis-ci.com/calvinbui/ansible-docker.svg?branch=master)](https://travis-ci.com/calvinbui/ansible-docker)
![GitHub release](https://img.shields.io/github/release/calvinbui/ansible-docker.svg)
![Ansible Quality Score](https://img.shields.io/ansible/quality/35858.svg)
![Ansible Role](https://img.shields.io/ansible/role/d/35858.svg)

# Ansible Docker

An Ansible role that installs the latest version of Docker CE on Ubuntu based on the official installation instructions.

## Requirements

N/A

## Role Variables

`docker_users`: a list of users to add to the docker group. They will not be evaluated until a session is created.

## Dependencies

N/A

## Example Playbook

```yaml
- hosts: all
  become: true
  pre_tasks:
    - name: Update apt cache.
      apt:
        update_cache: true
        cache_valid_time: 600
      changed_when: false
  roles:
    - role: ansible-docker
```

## License

GPLv3

## Author Information

https://calvin.me
