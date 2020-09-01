# ansible_tibero
Ansible Role for Tibero Installation &amp; Configuration


- name: install tibero 
  hosts: tibero
  become: yes

  roles:
    - tibero
