# Alternatives and Difference between them

## Chef
### Introduction
- Chef ensures configrations are applied consistently in every environment, at any scale, with infrastructure automation
- Open Source tool developed by Opscode written in ruby and Erlang
- Best suited for organiztions that have heterogenous infrastructure aand are looking or mature solution.

### Architecture

### Pro and Cons
**Pros**
- Large Collections of receipes are available
- Integrates well with Git which provides a strong version control
  
**Cons**
- A considerable amount of learning time is required if one is not confortable with ruby
- The main server doesn't have much control

---
## Puppet
### Introduction
- Puppet is a configration management tools that supports automatic deployments
- Built in Ruby and uses DSL (Domain Specific Language) for writing manifests
- Also works well with heterogenous environment where the focus is scalibility

### Architecture

### Pros and Cons
**Pros**
- Strong community support by Puppet Labs
- Well developed reporting mechanism

**Cons**
- For performing advance tasks, a good knowledge of Ruby is needed
- The main server doesn't have much controls

---
## Ansible
### Introduction
- Ansible is an IT automation tool that automates configuration management, cloud provisioning, deployment and orchestration
- The core of Ansible, playbooks, are written in YAML
- Works well with environments where the focus is on getting the servers up and running quickly


### Architecture

### Pros and Cons
**Pros**
- Agents need not be installed on system that requires configuration
- YAML is extremely easy to understand and learn

**Cons**
- Performance speed is often less than other tools
- YAML is not as powerful as most languages

---
## SaltStack

### Introduction
- CLI based tool that automates configuration management and remote execution
- It is Python based while the instructions are written in YAML or it's DSL
- It is perfect for an environment with scalibility and resilience as its priority

### Architecture

### Pros and Cons
**Pros**
- Extremely simple usage once it's set up
- A good reporting mechanism that allows one to easily view all operations

**Cons**
- Setup phase is slightly tougher
- Relatively new web UI which is much less developed as compared to other tools

___
|   | Chef | Puppet | Ansible | SaltStack  |
|---|---|---|---|---|
| Architecture | Server/Client | Server/Client | Client Only | Server/Client |
| Ease of Setup | Moderate | Moderate | Very Easy | Moderate |
| Language | Procedural: Specify how to do task | Declarative: specify only what to do | Procedural: Specify how to do task | Declarative: specify only what to do |
| Scalability | Scalable | Scalable | Scalable | Scalable |
| Management | Tough as it requires one to learn Ruby(DSL) | Tough as it requires one to learn Puppet DSL | Very Easy | Very Easy |
| Interoperabilty | High | High | High | High |
| Cloud availability | Amazon | Amazon, Aure | none | none |
| Communication | Knife tool | SSL | SSH | SSH |


Each tool has its pros and cons and each serve specific environment requirements