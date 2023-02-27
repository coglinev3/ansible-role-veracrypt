# Ansible Role: veracrypt

[![Build](https://github.com/coglinev3/ansible-role-veracrypt/actions/workflows/build.yml/badge.svg)](https://github.com/coglinev3/ansible-role-veracrypt/actions/workflows/build.yml) ![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/coglinev3/ansible-role-veracrypt) [![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://raw.githubusercontent.com/coglinev3/ansible-role-veracrypt/master/LICENSE)

This Ansible role installs [VeraCrypt](https://www.veracrypt.fr/ "VeraCrypt"), a free open source disk encryption software.
The following Linux distributions are supported:

* Debian 9 (Stretch),
* Debian 10 (Buster),
* Debian 11 (Buster),
* Enterprise Linux 7, 
* Enterprise Linux 8, 
* Fedora 35,
* Fedora 36,
* Fedora 37,
* Ubuntu 16.04 LTS (Xenial Xerus),
* Ubuntu 18.04 LTS (Bionic Beaver),
* Ubuntu 20.04 LTS (Focal Fossa),
* Ubuntu 22.04 LTS (Jammy Jellyfish).

This Role was tested with [GitHub Actions](https://github.com/features/actions "GitHub Actions") using [Ansible Molecule](https://molecule.readthedocs.io/en/latest/# "Ansible Molecule Documentation") and with a [multi virtual machine veracrypt environment](https://ansible-development.readthedocs.io "Environment for developing and testing Ansible roles").

## Requirements

None


## Role Variables

Available variables are listed below, along with default values:

```yml
# packages to be installed
veracrypt_packages:
  - veracrypt

# default packages state: (present) | latest | absent 
veracrypt_packages_state: present
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

Release: 1.2.0


## License

BSD


## Author Information

Copyright &copy; 2022 Cogline.v3.
