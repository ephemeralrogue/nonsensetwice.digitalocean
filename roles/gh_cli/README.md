gh_cli
=========

Installs the GitHub CLI on Ubuntu 22.04

Requirements
------------

This role requires that a server be initialized with a non-root user with passwordless sudo permissions.

Role Variables
--------------

No variables are necessary to use this role.

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
    - nonsensetwice.digitalocean.gh_cli
```
at the task level as a dynamic import:
```
---
- hosts: all

  tasks:
    - name: Install Docker
    include_role: nonsensetwice.digitalocean.gh_cli
```
as a static import:
```
---
- hosts: all

  tasks:
    - name: Install Docker
      import_role: nonsensetwice.digitalocean.gh_cli
```

License
-------

MIT

Author Information
------------------

Written by nonsensetwice
[GitHub](https://github.com/nonsensetwice)
[Twitter](https://twitter.com/nonsensecodes)