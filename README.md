# Ansible Role: veracrypt

[![Build](https://github.com/coglinev3/ansible-role-veracrypt/actions/workflows/build.yml/badge.svg)](https://github.com/coglinev3/ansible-role-veracrypt/actions/workflows/build.yml) ![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/coglinev3/ansible-role-veracrypt) [![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://raw.githubusercontent.com/coglinev3/ansible-role-veracrypt/master/LICENSE)

This Ansible role installs [VeraCrypt](https://www.veracrypt.fr/ "VeraCrypt"),
a free open source disk encryption software.

This version is a complete redesign of the role to install the original
os specific package provided by the author [IDRIX](https://www.idrix.fr).

The following Linux distributions are supported:

* Debian 10 (Buster),
* Debian 11 (Buster),
* Enterprise Linux 7, 
* Enterprise Linux 8, 
* Enterprise Linux 9, 
* Fedora 35,
* Fedora 36,
* Fedora 37,
* Fedora 38,
* Fedora 39,
* Ubuntu 20.04 LTS (Focal Fossa),
* Ubuntu 22.04 LTS (Jammy Jellyfish).

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

Release: 1.3.1


## License

BSD


## Author Information

Copyright &copy; 2023 Cogline.v3.
