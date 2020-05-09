# Ansible Role: Docker
Ansible role that installs Docker and Docker Compose.

**Supported Platforms:**
- Arch Linux
- Debian buster

## Requirements
To install Docker Compose on Debian, Python pip is required.

## Role Variables
| Variable           | Default | Description                                                         |
|:-------------------|:--------|:--------------------------------------------------------------------|
| **docker_compose** | `true`  | Whether to install docker compose.                                  |
| **pip_executable** | `pip3`  | The pip executable to use when installing docker compose on Debian. |
| **docker_users**   | `[]`    | A list of users that should be added to the docker group.           |

## Dependencies
None.

## Example Playbook

```yaml
- hosts: docker
  gather_facts: yes # required for os detection
  roles:
    - role: acehko.docker
      docker_compose: true
      pip_executable: pip3
      docker_users:
        - user1
        - user2
```

## License
[MIT](LICENSE)

## Author Information
[Andrija Čehko](https://github.com/acehko)
