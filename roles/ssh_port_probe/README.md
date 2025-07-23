# ansible-ssh-port-probe

[![Ansible Molecule Test Matrix](https://github.com/nfaction/ansible-ssh-port-probe/actions/workflows/molecule.yml/badge.svg)](https://github.com/nfaction/ansible-ssh-port-probe/actions/workflows/molecule.yml)

Test ssh port(s) and install a one or more ssh keys for future logins

## Usage

Use the playbook in this role to probe ssh ports and install ssh keys.

### Add key to standard user

``` bash
ansible-playbook <roles-path>/ansible-ssh-port-probe/ssh-port-probe.yml \
  -vvv -i <ip-of-host>, -k -u <username>
```

### Add key to root user

Be sure to pass `-K` and `-k` in order to prompt for `ssh` password and `sudo` password. *Note:* User must be in `/etc/sudoers` or similar before running this playbook.

``` bash
ansible-playbook galaxy-roles/ansible-ssh-port-probe/ssh-port-probe.yml \
  -vvv -i <ip-of-host>, -k -u <username> -K \
  -e ssh_key_user=root \
  -e ssh_key_sudo=true
```

## Variables

* `ssh_key_user`: user to install ssh keys. E.g. `/home/<user>/.ssh/authorized_keys`.
* `ssh_key_sudo` if true, will elevate to `root` and install ssh key for `ssh_key_user`.
