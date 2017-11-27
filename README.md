ansible-role-nginx
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-nginx.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-nginx)

Add nginx to your machine.

Requirements
------------

Systems running this playbook should have access to a repository containing nginx.

Role Variables
--------------

- appport - You can specify what port should be used to listen on. The default (defaults/main.yml) is port 80.

Dependencies
------------

- robertdebock.ansible-role-epel

Download the dependencies by issueing this command:
```
ansible-galaxy install --role-file requirements.yml
```

Example Playbook
----------------

```
- hosts: all

  roles:
    - role: robertdebock.ansible-role-nginx
      appport: 8080

  tasks:
    - name: place some content
      copy:
        src: files/index.html
        dest: /usr/share/nginx/html/index.html
```

Install this role using `galaxy install robertdebock.ansible-role-nginx`.

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock <robert@meinit.nl>
