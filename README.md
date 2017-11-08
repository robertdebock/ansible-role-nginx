nginx
=========

A role that adds nginx

Requirements
------------

Systems running this playbook should have access to a repository containing nginx.
- robertdebock.epel

Role Variables
--------------

- port - You can specify what port should be used to listen on. The default (defaults/main.yml) is port 80.

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
