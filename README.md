Install MySql
=========

Ansible role to install and configure MySQL

Requirements
------------

RedHat 6, 7

Role Variables
--------------

`mysql_packages: []` list of packages to install for mysql.

Dependencies
------------


Example Playbook
----------------

Example on how to include this role into your playbook

    - hosts: servers
      roles:
         - { role: username.rolename,
              mysql_packages:[
                "mysql",
                "mysql-server"
              ]
           }

License
-------

MIT

Author Information
------------------

Find me on github [@BondAnthony](https://github.com/BondAnthony)