```
 ├── <roles name>
    │   ├── defaults
    │   │   └── main.yml
    │   ├── files
    │   ├── handlers
    │   │   └── main.yml
    │   ├── meta
    │   │   └── main.yml
    │   ├── README.md
    │   ├── tasks
    │   │   └── main.yml
    │   ├── templates
    │   ├── tests
    │   │   ├── inventory
    │   │   └── test.yml
    │   └── vars
    │       └── main.yml
```

- can be created by just a simple command ```ansible-galaxy init <rolename>```
- default/main.yml:
  - contains the default variables.
- files:
  - contains the files for the role use
  - contains the files used in the role
- handlers/main.yml:
  - contains the handlers used in the role
  - handlers are the code run after a task when it is notified.
- README.md:
  - Markdown file contain the info for the role
- tasks/main.yml:
  - contains the tasks that are imported to the playbook when role is used
- templates:
  - contains the temlates used by the role
  - generally the jinja2 templates
  - uses the variable values used in the template for the file that ansible used to create on managed nodes
- test:
  - test.yml
    - playbook to test the role
  - inventory
    - used to define the IPs to test role onto.
- vars/main.yml