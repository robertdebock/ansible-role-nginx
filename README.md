nginx
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-nginx.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-nginx)

Add nginx to your machine.

Context
--------
This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/robertdebock.github.io/artifacts/nginx.png "Dependency")

Requirements
------------

Systems running this playbook should have access to a repository containing nginx.

Role Variables
--------------

- nginx_port - You can specify what port should be used to listen on. The default (defaults/main.yml) is port 80.

Dependencies
------------

These roles prepare your system to use this role on them.

- [robertdebock.bootstrap](https://travis-ci.org/robertdebock/ansible-role-bootstrap)
- [robertdebock.epel](https://travis-ci.org/robertdebock/ansible-role-epel)

Download the dependencies by issuing this command:
```
ansible-galaxy install --role-file requirements.yml
```

Compatibility
-------------

This role has been tested against the following distributions and Ansible version:

|distribution|ansible 2.3|ansible 2.4|ansible 2.5|
|------------|-----------|-----------|-----------|
|alpine-3.6|yes|yes|yes|
|alpine-3.7|yes|yes|yes|
|archlinux|yes|yes|yes|
|centos-6|yes|yes|yes|
|centos-7|yes|yes|yes|
|debian-buster|yes|yes|yes|
|debian-stretch|yes|yes|yes|
|debian-wheezy|yes|yes|yes|
|fedora-27|yes|yes|yes|
|fedora-28|yes|yes|yes|
|opensuse-42.2|yes|yes|yes|
|opensuse-42.3|yes|yes|yes|
|ubuntu-artful|yes|yes|yes|
|ubuntu-bionic|yes|yes|yes|

Example Playbook
----------------

```
- hosts: all

  roles:
    - role: robertdebock.bootstrap
    - role: robertdebock.epel
    - role: robertdebock.nginx
      appport: 8080

  tasks:
    - name: place some content
      copy:
        src: files/index.html
        dest: /usr/share/nginx/html/index.html
```

Install this role using `galaxy install robertdebock.nginx`.

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock](https://robertdebock.nl/) <robert@meinit.nl>
