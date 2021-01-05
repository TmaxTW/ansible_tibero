# ansible_tibero
Ansible Role for Tibero Installation &amp; Configuration


## Download Tibero binary package and request demo license
- https://technet.tmaxsoft.com

## playbook
```
- name: install tibero 
  hosts: tibero
  become: yes

  roles:
    - tibero
```
