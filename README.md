Ansible DB-pull role
====================

Sync local PostgreSQL or MySQL database with remote.

Requirements
------------

The local system need to have either `pg_dump` and `pg_reload` command or `mysql` and `mysqldump`.

Role Variables
--------------

The `defaults` vars declared in this module:

```
db_pull_remote_backup_path: /tmp/db-pull
db_pull_local_backup_path: /tmp/db-pull
db_pull_keep_backup: 5

db_pull_remote_database_user: postgres
db_pull_remote_database_host: localhost
db_pull_remote_database_name: postgres
db_pull_remote_database_password: root
db_pull_remote_database_port: 5432

db_pull_local_database_user: postgres
db_pull_local_database_host: localhost
db_pull_local_database_name: postgres
db_pull_local_database_password: root
db_pull_local_database_port: 5432

db_pull_database_type: postgres

db_pull_skip_restore: false

db_pull_exclude_table: []
db_pull_exclude_table_data: []
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: db-pull }

License
-------

MIT

Author Information
------------------

 * ansible-db-pull, written by Erwan Richard
