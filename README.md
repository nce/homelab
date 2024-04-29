# Ansible
I'll try to gather all my automations/server setups here

#### Homepage Icons
* https://pictogrammers.com/library/mdi/
* https://github.com/walkxcode/dashboard-icons/tree/main

## Home
All homeserver/home related IT stuff

### home:t8

#### Initial Setup
Currently provisioned with debian12

1. Default user account ssh setup
```bash
mkdir .ssh
chmod 700 .ssh
wget -o .ssh/authorized_keys github.com/nce.keys
chmod 600 .ssh/authorized_keys
```
2. Ansible requirements
```bash
apt install sudo
echo "nce ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
```

### Run Ansible
```bash
# Limited to this machine
ansible-playbook -l t8 site.yaml
```
