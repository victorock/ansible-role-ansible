Ansible Role to Install KSM
=========

Ansible role to install Kernel Same-Page Merging.

Role Variables
--------------

Variables are defined in `defaults/main.yml` as well as `vars/`. Based on the operating system family, version, and installation method, variables will be set the appropriate values.

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `autorun` | `False`  | Boolean to define if the role "autorun". Useful when you want to have dependencies solved by galaxy (`meta/main.yml`) but don't want it to run automatically.  |
| `ksm_services_state` | `started`  | The services state: running, stopped or restarted |
| `ksm_services_enabled` | `yes` | Bool to define if services shall start on-boot. |


Examples
------------

Follow below different examples and ways to use this role.

>Playbook: Install KSM

```YAML
---
- name: "ksm: Install KSM"
  hosts: libvirt
  gather_facts: false
  become: true

  roles:
    - role: victorock.ksm
      autorun: true

```

Dependencies
------------

None

Requirements
------------

Server configured with repository containing ksm package.

Example role to install epel:
- geerlingguy.repo-epel

Example role using RHSM:
- victorock.linux

License
------------

GPLv3

Author
------------

Victor da Costa (@victorock)
