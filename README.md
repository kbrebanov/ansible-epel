epel
====

Installs and configures Yum EPEL repository.

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

    # EPEL download URL's.
    epel_url_6: http://download.fedoraproject.org/pub/epel/6/i386/epel-release-6-8.noarch.rpm
    epel_url_7: http://download.fedoraproject.org/pub/epel/7/x86_64/e/epel-release-7-2.noarch.rpm

    # Enable EPEL repo
    epel_repo_enabled: 1
    # Enable EPEL debuginfo repo
    epel_repo_debuginfo_enabled: 0
    # Enable EPEL source repo
    epel_repo_source_enabled: 0

    # Enable EPEL testing repo
    epel_repo_testing_enabled: 0
    # Enable EPEL testing debuginfo repo
    epel_repo_testing_debuginfo_enabled: 0
    # Enable EPEL testing source repo
    epel_repo_testing_source_enabled: 0

Dependencies
------------


Example Playbook
----------------

1) Install and enable EPEL repo

    - hosts: all
      roles:
         - { role: epel }

2) Install and disable EPEL repo

    - hosts: all
      roles:
         - { role: epel, epel_repo_enabled: 0 }

License
-------

BSD

Author Information
------------------

Kevin Brebanov
