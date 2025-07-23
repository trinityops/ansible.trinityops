# ansible-bootstrap

[![Ansible Molecule Test Matrix](https://github.com/nfaction/ansible-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/nfaction/ansible-bootstrap/actions/workflows/molecule.yml)

Role to bootstrap systems/hosts

## Usage

Run this role:

``` bash
ansible-playbook -i localhost, bootstrap.yml -vvv
```

### Variables

``` bash
# Example of how to install downloaded packages
dl_packages_to_install:
  - name: google-chrome debian
    url: "https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb"
    binary_type: deb
    path: "{{ dl_packages_path }}/google-chrome-stable_current_amd64.deb"
```
