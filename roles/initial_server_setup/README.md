initial_server_setup
=========

This role initializes a new server with a non-root user using passwordless sudo.

Requirements
------------

There are no prerequisites to using this role.

Role Variables
--------------

`create_user` is set via the `CREATED_USERNAME` environment variable in `vars/main.yml`. You can set this variable with:
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
    - nonsensetwice.digitalocean.initial_server_setup
```
at the task level as a dynamic import:
```
---
- hosts: all

  tasks:
    - name: Install Docker
    include_role: nonsensetwice.digitalocean.initial_server_setup
```
as a static import:
```
---
- hosts: all

  tasks:
    - name: Install Docker
      import_role: nonsensetwice.digitalocean.initial_server_setup
```

License
-------

MIT

Author Information
------------------

Written by nonsensetwice
[GitHub](https://github.com/nonsensetwice)
[Twitter](https://twitter.com/nonsensecodes)