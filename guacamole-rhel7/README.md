Role Name
=========

guacamole setup for rhel7.

I would give crdit to the originator but don't recall and didn't branch.
I had to do alot of work to get this functional (don't know if it becuse obsolete or rhel7 or what)

Requirements
------------

ansible user with with become 'see inventory file with everything needed' 

Role Variables
--------------

'see defaults file with everything'
Depending on the versions the following are functional
select MySQL (mariadb) or PostgreSQL (default)

guacamole_version: 1.4.0
guacamole_postgresql_auth: true
guacamole_postgresql_connector_version: 42.2.20
guacamole_mysql_auth: false
guacamole_mysql_connector_version: 8.0.13

Dependencies
------------

ansible user with with become 'see inventory file with everything needed' 
rhel7/centos7 with access to internet (lots of pulling src/bin/repos) 
- base repos
- extra repo (installed)
- rpmfusion repo (installed)


Example Playbook
----------------

'nothing special'

ansible-playbook -i inventory test.yml

cat test.yml
---
- name: guacamole-rhel7
  hosts: guachosts
  tasks:
    - name: Include guacamole-rhel7
      include_role:
        name: guacamole-rhel7

License
-------

BSD

Author Information
------------------

ricksanchezc8675309@gmail.com
