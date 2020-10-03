Ansible.Role.System.IdentityManagement
=========

Rola zakładająca i usuwająca grupy systemowe

Język: [EN](README.md), [PL](README.PL.md)

Zmiene w Roli:
--------------
requires:
```
    groups_on_host: # List group do założenie i/lub usunięcia
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

Przykładowy Playbook
----------------

Przykładowe użycie roli
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

Testowane
------------

Testing on:
  - Ubuntu 16.04 LTS
  - Ubuntu 18.04 LTS
  - Ubuntu 20.04 LTS
  - Centos 7
  - Centos 8

Licencja
-------

BSD

Autor
------------------
 **Maciej Rachuna**
##### System Administrator & DevOps Engineer
rachuna.maciej@gmail.com