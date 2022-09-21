# Re-using Ansible artifacts

- We can write a simple playbook in one very large file, and most users learn the one-file approach first. 
- However, breaking your automation work up into smaller files is an excellent way to organize complex sets of tasks and reuse them. 
- Smaller, more distributed artifacts let you re-use the same variables, tasks, and plays in multiple playbooks to address different use cases. 
- We can use distributed artifacts across multiple parent playbooks or even multiple times within one playbook. 
- For example, you might want to update your customer database as part of several different playbooks. If you put all the tasks related to updating your database in a tasks file or a role, you can re-use them in many playbooks while only maintaining them in one place.

### Creating re-usable files and roles
- Ansible offers four distributed, re-usable artifacts: variables files, task files, playbooks, and roles.
- A variables file contains only variables.
- A task file contains only tasks.
- A playbook contains at least one play, and may contain variables, tasks, and other content. You can re-use tightly focused playbooks, but you can only re-use them statically, not dynamically.
- A role contains a set of related tasks, variables, defaults, handlers, and even modules or other plugins in a defined file-tree. Unlike variables files, task files, or playbooks, roles can be easily uploaded and shared via Ansible Galaxy. For details about [creating and using roles](./Ansible%20Role.md).


### Re-using playbooks
We can incorporate multiple playbooks into a main playbook. However, we can only use imports to re-use playbooks. For example:
```
- import_playbook: webservers.yml
- import_playbook: databases.yml
```

### Re-using files and roles
Ansible offers two ways to re-use files and roles in a playbook: dynamic and static.

- For dynamic re-use, add an include_* task in the tasks section of a play:
  - include_role
  - include_tasks
  - include_vars

- For static re-use, add an import_* task in the tasks section of a play:
  - import_role
  - import_tasks

Task include and import statements can be used at arbitrary depth.

>You can still use the bare roles keyword at the play level to incorporate a role in a playbook statically. However, the bare include keyword, once used for both task files and playbook-level includes, is now deprecated.


References:
- https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse.html
- 