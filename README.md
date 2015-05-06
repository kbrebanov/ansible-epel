epel
====

[![Ansible Galaxy](https://img.shields.io/badge/galaxy-kbrebanov.epel-660198.svg)](https://galaxy.ansible.com/list#/roles/3290)

Installs and configures Yum EPEL repository.

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name                                | Default | Description                                |
|-------------------------------------|---------|--------------------------------------------|
| epel_repo_enabled                   | true    | Enable/disable EPEL repo                   |
| epel_repo_debuginfo_enabled         | false   | Enable/disable EPEL debuginfo repo         |
| epel_repo_source_enabled            | false   | Enable/disable EPEL source repo            |
| epel_repo_testing_enabled           | false   | Enable/disable EPEL testing repo           |
| epel_repo_testing_debuginfo_enabled | false   | Enable/disable EPEL testing debuginfo repo |
| epel_repo_testing_source_enabled    | false   | Enable/disable EPEL testing source repo    |

Dependencies
------------

None

Example Playbook
----------------

Install and enable EPEL repo
```
- hosts: all
  roles:
    - { role: kbrebanov.epel }
```

Install and disable EPEL repo
```
- hosts: all
  roles:
    - { role: kbrebanov.epel, epel_repo_enabled: false }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
