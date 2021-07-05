# ansible_tibero
Ansible Role for Tibero Installation &amp; Configuration


## Download Tibero binary package and request demo license
- https://technet.tmaxsoft.com

## sample playbook - with hosts
```
- name: install tibero 
  hosts: tibero
  become: yes

  roles:
    - tibero
```

## sample playbook - local
```
- name: install tibero 
  hosts: localhost
  connection: local
  become: yes

  #- name: install tibero 
  #hosts: tibero
  #become: yes

  roles:
    - role: tibero
      vars: 
        tb_user: tibero
        tb_base: /opt/tmaxsoft
        tb_passwd: '$6$FpwzW7cBVP/3K2$CAWIA9PU49uKTexwTrLRDcO4LAiVOaCi4P3r6zGEn6DJhcXJwAwXMwlolPWMrdS6MT2x1faGjWXwWEnSv5Fog.'
        tb_pkg_name: "tibero6-bin-FS07_CS_2005-linux64-186930-opt-tested.tar.gz"
        tb_sys_passwd: tibero
        tb_group: dba
        tb_sid: tibero
        memory_target: 6G
        total_shm_size: 4G
        db_writer_count: 12
        log_buffer: 1G
        db_cache_size: 2G
        max_session_count: 100
        redo_size: 300M
        tb_listener_port: 8629
        db_character_set: UTF8
        #db_character_set: ZHT16MSWIN950
        db_national_charater_set: UTF16
```
