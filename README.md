Ansible Role to Install Ansible
=========

Ansible role to install Ansible by Red Hat.

Role Variables
--------------

Variables are defined in `defaults/main.yml` as well as `vars/`. Based on the operating system family, version, and installation method, variables will be set the appropriate values.

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `autorun` | `False`  | Boolean to define if the role "autorun". Useful when you want to have dependencies solved by galaxy (`meta/main.yml`) but don't want it to run automatically.  |
| `ansible_version` | `2.6`  | The Ansible version to install. |
| `ansible_release` | `yes`  | Boolean to enable `release` repo. |
| `ansible_preview` | `no`  | Boolean to enable `preview` repo. |

Examples
------------

Follow below different examples and ways to use this role.

>Playbook: Install Ansible

```YAML
---
- name: "ansible: Install Ansible"
  hosts: hosts
  gather_facts: false
  become: true

  roles:
    - role: victorock.ansible
      autorun: true

```

Dependencies
------------

None

Requirements
------------

None

License
------------

GPLv3

Author
------------

Victor da Costa (@victorock)
