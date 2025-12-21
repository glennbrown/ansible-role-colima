# ansible-role-colima

Role to install Colima, Docker and related Homebrew packages on macOS.

Usage
-----

Include this role in your playbook:

```yaml
- hosts: localhost
  connection: local
  roles:
    - role: glennbrown.ansible-role-colima
```

Variables
---------

- `colima_packages` (list): packages installed via Homebrew. Defaults to:

  - colima
  - lima-additional-guestagents
  - docker
  - docker-compose
  - docker-buildx
  - docker-completion

Notes
-----

- This role uses the `community.general.homebrew` module; ensure the collection is available.
- The role asserts it is running on macOS (Darwin).
# ansible-role-colima
Ansible Role to install and configure colima on macOS
