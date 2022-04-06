Helm
=========

Ansible Role to install Helm

Requirements
------------

Install [`kubernetes.core`](https://docs.ansible.com/ansible/latest/collections/kubernetes/core/k8s_module.html) collection (version 2.2.2).

```bash
ansible-galaxy collection install kubernetes.core
```

Role Variables
--------------

```
# Helm version
helm_version: 3.8.1
```

Example Playbook
----------------

```yaml
- name: Ansible Playbook to install Helm
  hosts: all
  gather_facts: yes
  any_errors_fatal: true
  become: true
  roles:
    - role: helm
      tags:
        - helm
```

License
-------

MIT

Author Information
------------------

Ewerton Silva <ewerton116@gmail.com>
