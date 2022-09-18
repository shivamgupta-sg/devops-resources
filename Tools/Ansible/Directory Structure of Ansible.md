```
|   ansible.cfg
|   hosts
|   group_vars
|   roles
|   playbooks
```
>That is a way to organize (especially when first getting accustomed with Ansible), not necessarily the way.  Ansible allows you to fully configure the inventory path, library path, role path, etc with either environment variables or using ansible.cfg

ansible.cfg: 
- Configration file of ansible
- Ansible search for the config in the current directory, if not found it by defaults consider the config file in ```/etc/ansible``` directory

host:
- contains IPs of the managed nodes
- can use multiple inventories by defining in the cli using the ```-i``` flag
- can be configured using ansible.cfg

group_vars:
- contains group variables used by the inventory groups

roles:
- can be used to store the roles used in the playbook
- can be configured by ansible.cfg
- ansible-galaxy can be used for the roles (ansible cli)

playbooks:
- generally used to store the playbooks