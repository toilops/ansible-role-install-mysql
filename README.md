Install MySql
=========

Ansible role to install and configure MySQL

Requirements
------------

RedHat 6, 7

Role Variables
--------------

`mysql_repo: url` url of the mysql repo rpm configurations.
`mysql_packages: []` list of packages to install for mysql.
`mysql_dirs: []` list of MySQL directories that are used by the application.
`mysql_unused_databases: []` list of MySQL databases that need to be dropped, example `test`.

Performance and tuning configurations are set within the `my.cnf` file. The role will template the file over to `/etc/my.cnf` on the remote server. Please review the `defaults/main.yml` file for variables related to the build of `my.cnf`. Review the `### Begin: MySQL Tuning  ###`.

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
I have to give a lot of credit to [@Geerlingguy](https://github.com/geerlingguy) since he has already done a lot of this work.