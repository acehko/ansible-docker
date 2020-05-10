# Ansible Role: Docker
[![Build Status](https://travis-ci.com/acehko/ansible-docker.svg?branch=master)](https://travis-ci.com/acehko/ansible-docker)

Ansible role that installs Docker and Docker Compose.

## Supported Platforms
- Arch Linux
- Debian buster

## Requirements
- **gather_facts** is required for OS detection.
- Python 3. Python 2 is not supported.

## Role Variables
| Variable            | Default | Description                                                          |
|:--------------------|:--------|:---------------------------------------------------------------------|
| **docker_compose**  | `true`  | Whether to install docker compose.                                   |
| **docker_users**    | `[]`    | A list of users that should be added to the docker group.            |
| **ansible_modules** | `false` | Whether to install packages required for the ansible docker modules. |

## Dependencies
None.

## Example Playbook

```yaml
- hosts: all
  gather_facts: true
  roles:
    - role: acehko.docker
      docker_compose: true
      docker_users:
        - user1
        - user2
```

## License
[MIT](LICENSE)

## Author Information
[Andrija Čehko](https://github.com/acehko)
