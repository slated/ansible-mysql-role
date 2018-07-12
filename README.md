[![Build Status](https://travis-ci.org/slated/ansible-mysql-role.svg?branch=master)](https://travis-ci.org/slated/ansible-mysql-role)

MySQL
==========

Add MySQL official Apt repo, optionally install and configure
client and/or server. (Server not yet implemented.) By default, only
the repo is added; see _Role Variables_.

Requirements
------------

An installed Ubuntu server. 

Role Variables
--------------

Do or do not install the Mysql client, server. Not that by
default we only add the apt.mysql.org repo.

    mysql_install_client: no
    mysql_install_server: no


Dependencies
------------

None.

Example Playbook
----------------

    - hosts: dbservers
      tasks:
        - import_role:
            name: mysql
          vars:
            mysql_install_client: yes
            mysql_install_client: no
