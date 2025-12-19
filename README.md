# Ansible Role: veracrypt

[![Build](https://github.com/coglinev3/ansible-role-veracrypt/actions/workflows/build.yml/badge.svg)](https://github.com/coglinev3/ansible-role-veracrypt/actions/workflows/build.yml) ![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/coglinev3/ansible-role-veracrypt) [![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://raw.githubusercontent.com/coglinev3/ansible-role-veracrypt/master/LICENSE)

This Ansible role installs [VeraCrypt](https://www.veracrypt.fr/ "VeraCrypt"),
a free open source disk encryption software.

This version is a complete redesign of the role to install the original
os specific package provided by the author [IDRIX](https://www.idrix.fr).

The following Linux distributions are supported:

* Debian 11 (Bullseye),
* Debian 12 (Bookworm),
* Debian 13 (Trixie),
* Enterprise Linux 9, 
* Enterprise Linux 10, 
* Ubuntu 22.04 LTS (Jammy Jellyfish),
* Ubuntu 24.04 LTS (Noble Numbat).

This Role was tested with [GitHub Actions](https://github.com/features/actions
"GitHub Actions") using [Ansible
Molecule](https://ansible.readthedocs.io/projects/molecule/ "Ansible Molecule
Home").

## Requirements

None


## Role Variables

Available variables are listed below, along with default values:

```yml
# Define dependencies
veracrypt_dependencies: []

# Install latest VeraCrypt version: latest | specific version e.g. 1.26.7
# If you want to use existinig TrueCrypt containers, then you should use
# version 1.25.9. This is the latest version with TrueCrypt support.
veracrypt_package_version: latest

# default package states: present | latest | absent
veracrypt_package_state: present

# Install GUI or console only version: true | false
veracrypt_package_console_only: false
```

## Dependencies

None


## Example Playbook

```yml
---
# file: tests/test.yml

- hosts: local
  roles:
    - { role: coglinev3.veracrypt }
```

## Version

Release: 2.0.1


## License

BSD


## Author Information

Copyright &copy; 2024 Cogline.v3.
