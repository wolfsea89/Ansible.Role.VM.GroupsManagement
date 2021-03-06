Ansible.Role.System.IdentityManagement
=========

This role creates system groups

Language: [EN](README.md), [PL](README.PL.md)

Role Variables
--------------
requires:
```
    groups_on_host: # List group on serwer
```

var `groups_on_host` example:
```
groups_on_host:
    - name: adm
      state: present
    - name: sudo
      state: present
    - name: testers
      state: absent
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
- hosts: localhost
  remote_user: root
  become: true
  gather_facts: yes
  roles:
    - role: Ansible.Role.System.GroupManagement
      vars:
        groups_on_host:
          - name: adm
            state: present
          - name: sudo
            state: present
          - name: testers
            state: absent
```

Testing
------------

Testing on:
  - Ubuntu 16.04 LTS
  - Ubuntu 18.04 LTS
  - Ubuntu 20.04 LTS
  - Centos 7
  - Centos 8

License
-------

BSD

Author Information
------------------
 **Maciej Rachuna**
##### System Administrator & DevOps Engineer
rachuna.maciej@gmail.com
