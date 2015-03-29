# ansible-role.base

Install
========
```
git submodule add git@github.com:Waldz/ansible-role.base.git roles/base
```

Example
========
```
- name: Basic configuration to all servers
  hosts: all
  sudo: true
  roles:
    - role: base
  vars:
    - deploy_key: vars/deploy_key/id_dsa
    - deploy_user: www-data
    - auth_users:
      - name: valdas
        comment: "Valdas Petrulis"
        #groups: "adm"
    - auth_keys:
      - user: valdas
        key: ~/.ssh/id_rsa.pub
```
