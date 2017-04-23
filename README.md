# Ansible Role: Mysql setup

Sets up mysql directories. This role is mainly for use prior to running a mysql server in a docker container, with the mysql directories mounted as volumes. This role does not install the mysql server itself.

Role Variables
--------------

Ansible variables are listed below with their default values.

```
mysql_backups_dir: /var/mysql/backups
mysql_conf_dir: /var/mysql/conf.d
mysql_lib_dir: /var/mysql/lib

mysql_character_set: utf8mb4
mysql_collation: utf8mb4_unicode_520_ci

mysql_user: mysql
```

Example Playbook
----------------

```
---
- hosts: webservers
  roles:
  	- opichon.mysql-setup
```

License
-------

MIT
