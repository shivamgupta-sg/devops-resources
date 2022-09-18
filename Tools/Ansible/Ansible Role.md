#Ansible Role

###What is a Ansible role?
- Roles provide a framework for fully independent, or interdependent collections of variables, tasks, files, templates, and modules.
- In Ansible, the role is the primary mechanism for breaking a playbook into multiple files. 
- This simplifies writing complex playbooks, and it makes them easier to reuse. 
- The breaking of playbook allows you to logically break the playbook into reusable components.
- Each role is basically limited to a particular functionality or desired output, with all the necessary steps to provide that result either within that role itself or in other roles listed as dependencies.
- Roles are not playbooks. Roles are small functionality which can be independently used but have to be used within playbooks. 
- There is no way to directly execute a role. 
- Roles have no explicit setting for which host the role will apply to.
- Top-level playbooks are the bridge holding the hosts from your inventory file to roles that should be applied to those hosts.

###Creating a New Role
- The directory structure for roles is essential to create a new role.
- Roles have a structured layout on the file system. 
- The default structure can be changed but for now let us stick to defaults.
- Each role is a directory tree in itself. 
- The role name is the directory name within the /roles directory.

```$ ansible-galaxy -h``` 

#### Usage
```ansible-galaxy [delete|import|info|init|install|list|login|remove|search|setup] [--help] [options] ... ```
####Options
- -h, --help − Show this help message and exit.

- -v, --verbose − Verbose mode (-vvv for more, -vvvv to enable connection debugging)

- --version − Show program's version number and exit.

