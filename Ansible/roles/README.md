RDS-MSSQL
=========

Deploy AWS RDS MSSQL

Requirements
------------
Ansible host 2.4

Role Variables
--------------
settings.ini
security_group.yml
grant_priv.sql


Dependencies
------------

sqlcmd

Example Playbook
----------------


    - hosts: localhost
      roles:
         - { role: username.rolename, x: 42 }

License
-------

CC BY-NC-ND

Author Information
------------------

NRCH
