# Ansible Role: QEMU
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit)](https://github.com/pre-commit/pre-commit)

This role installs and customizes QEMU on Debian-based Linux systems. It:
 - Ensures that QEMU (Quick EMUlator) is installed
 - Ensures that KVM (a Linux kernel module) is installed and loaded

## Role Variables
See [defaults/main.yml](./defaults/main.yml) for a comprehensive list of role variables.  
Some of the most pertinent variables are:
- `qemu_user`

## Testing
Testing is performed using Molecule.  
See the [molecule](./molecule/) directory for more information.

## Linting
Linting is done automatically via [https://pre-commit.com/](https://pre-commit.com/).  
After setting up a virtual environment and installing `requirements.txt`, run  
`pre-commit run --all-files`  
See: https://github.com/ansible/ansible-lint  
See: https://github.com/pre-commit/pre-commit

## Example Playbook
    - hosts: servers
      vars_files:
        - vars/main.yml
      roles:
        - librick.qemu

*Inside `vars/main.yml`*:

    qemu_user: johndoe

## License

MIT Licensed

## Author Information

This role was created in 2023 by [Eric McDonald](https://juniperspring.xyz/).
