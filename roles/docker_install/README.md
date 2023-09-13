docker_install
=========

This will install Docker and docker-compose on Ubuntu 22.04 and add the non-root user to the `docker` group. 

Requirements
------------

This role requires that a server be initialized with a non-root user with passwordless sudo permissions.

Role Variables
--------------

`alter_user` is set via the `CREATED_USERNAME` environment variable in `vars/main.yml`. You can set this variable with:
```
export CREATED_USERNAME=value
```
or permanently set it by adding it to `~/.profile`.

Dependencies
------------

No dependencies are required to use this role.

Example Playbook
----------------

This is pretty straightforward use; simply use the fully qualified collection name (FQCN) to call the role ...
at the play level using the `roles` keyword:
```
---
- hosts: all
  roles:
    - nonsensetwice.digitalocean.docker_install
```
at the task level as a dynamic import:
```
---
- hosts: all

  tasks:
    - name: Install Docker
    include_role: nonsensetwice.digitalocean.docker_install
```
as a static import:
```
---
- hosts: all

  tasks:
    - name: Install Docker
      import_role: nonsensetwice.digitalocean.docker_install
```

License
-------

MIT

Author Information
------------------

Written by nonsensetwice
[GitHub](https://github.com/nonsensetwice)
[Twitter](https://twitter.com/nonsensecodes)
