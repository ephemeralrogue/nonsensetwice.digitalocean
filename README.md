# Ansible Collection - nonsensetwice.digitalocean

this collection houses a set of roles and playbooks for automating the setup of servers over a set of standard Digital Ocean (DO) droplets running Ubuntu 22.04, and installing software for the development and execution of software. running it on other versions and systems may produce unexpected results.  
  
## roles  
  
the following roles are available:  
- initial_server_setup  
- docker_install  
- gh_cli  
- nvm_node_latest  

these are fairly self-explanatory: `initial_server_setup` will initialize an Ubuntu server with a non-root passwordless sudo user; `docker_install` will install Docker, docker-compose, and add the user to the `docker` group; `gh_cli` will install the GitHub CLI; and `nvm_node_latest` will install Node Version Manager (NVM) and then install the latest version of node.js through NVM.  

these can be called in a playbook by using the collection's fully-qualified collection name (FQCN) ...
- at the play level using the `roles` keyword:
```
---
- hosts: all
  roles:
    - nonsensetwice.digitalocean.inital_server_setup
    - nonsensetwice.digitalocean.docker_install
```
- or imported/included at the task level:
```
  tasks:
    - name: install docker
      nonsensetwice.digitalocean.docker_install
```

## playbooks  

there is currently one playbook available:  
- server_docker_gh_setup  

this playbook will run the `initial_server_setup`, `docker_install`, and `gh_cli` roles sequentially.  
