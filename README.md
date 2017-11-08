nginx
=========

A role that adds nginx

Requirements
------------

Systems running this playbook should have access to a repository containing nginx.
- robertdebock.epel

Role Variables
--------------

None known

Dependencies
------------

- robertdebock.epel

Example Playbook
----------------

```
- hosts: servers
  roles:
    - role: robertdebock.nginx
```

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock <robert@meinit.nl>
