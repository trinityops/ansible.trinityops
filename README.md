# ansible.trinityops

Ansible Collection

## Using this Collections

```shell
ansible-galaxy collection install trinityops.bootstrap
```

## Git Subtree

**First time only**

Adding Ansible roles from outside

```shell
# internal
git subtree add --prefix=roles/ssh_config git@github.com:nfaction/ansible-ssh-config.git master --squash
git subtree add --prefix=roles/bootstrap git@github.com:nfaction/ansible-bootstrap.git master --squash
git subtree add --prefix=roles/ssh_port_probe git@github.com:nfaction/ansible-ssh-port-probe.git master --squash
git subtree add --prefix=roles/ntp git@github.com:nfaction/ansible-ntp.git master --squash
git subtree add --prefix=roles/proxmox_config git@github.com:nfaction/proxmox-config.git master --squash
git subtree add --prefix=roles/systemd_docker git@github.com:nfaction/ansible-systemd-docker.git master --squash
# external
git subtree add --prefix=roles/docker https://github.com/lean-delivery/ansible-role-docker.git master --squash
```

Updating subtrees

```shell
# internal
git subtree pull --prefix=roles/ssh_config git@github.com:nfaction/ansible-ssh-config.git master --squash
git subtree pull --prefix=roles/bootstrap git@github.com:nfaction/ansible-bootstrap.git master --squash
git subtree pull --prefix=roles/ssh_port_probe git@github.com:nfaction/ansible-ssh-port-probe.git master --squash
git subtree pull --prefix=roles/ntp git@github.com:nfaction/ansible-ntp.git master --squash
git subtree pull --prefix=roles/proxmox_config git@github.com:nfaction/proxmox-config.git master --squash
git subtree pull --prefix=roles/systemd_docker git@github.com:nfaction/ansible-systemd-docker.git master --squash
# external
git subtree pull --prefix=roles/docker https://github.com/lean-delivery/ansible-role-docker.git master --squash
```

## Building the Collection

```shell
# Build this collection
ansible-galaxy collection build

# Publish to Ansible Galaxy
## API_TOKEN in GitHub creds.
ansible-galaxy collection publish trinityopsdev-bootstrap-1.0.0.tar.gz --token YOUR_API_TOKEN
```
