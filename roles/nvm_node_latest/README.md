nvm_node_latest
=========

This install the node version manager (nvm) on Ubuntu 22.04. It then installs the latest version of node.js via nvm.

Requirements
------------

This role requires that a server be initialized with a non-root user with passwordless sudo permissions.

Role Variables
--------------

No variables are called in this role's execution.

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
    - nonsensetwice.digitalocean.nvm_node_latest
```
at the task level as a dynamic import:
```
---
- hosts: all

  tasks:
    - name: Install Docker
    include_role: nonsensetwice.digitalocean.nvm_node_latest
```
as a static import:
```
---
- hosts: all

  tasks:
    - name: Install Docker
      import_role: nonsensetwice.digitalocean.nvm_node_latest
```

License
-------

MIT

Author Information
------------------

Written by nonsensetwice
[GitHub](https://github.com/nonsensetwice)
[Twitter](https://twitter.com/nonsensecodes)