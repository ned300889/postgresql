Role Name
=========

Simple PostgreSQL role to setup and initilaze the database on Ubuntu 18.04, 20.04 and Centos &


Role Variables
--------------
Default variables are below, feel free to update these on a playbook level for the desired version/architecture

    architecture: x86_64
    postgresVersion: 14

Dependencies
------------
To ensure the system can be worked on and is updated to latest spec please include the below.

    {role: ned300889.bootstrap}

Example Playbook
----------------

    - hosts: postgresqlDatabases
      become: true
      roles:
	 - { role: ned300889.bootstrap }
         - { role: ned300889.postgres }
      vars:
         - architecture: x86_64
         - postgresVersion: 14

License
-------

BSD

