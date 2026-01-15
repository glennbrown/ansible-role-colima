# Ansible Role: Colima for Docker on MacOS

Role to install Colima, Docker and related Homebrew packages on macOS.

Usage
-----

Include this role in your playbook:

```yaml
- hosts: localhost
  roles:
    - role: glennbrown.colima
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
