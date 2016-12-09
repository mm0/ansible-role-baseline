Ansible Role: Baseline v1.0
=====================

[![Build Status](https://travis-ci.org/mm0/ansible-role-baseline.svg?branch=master)](https://travis-ci.org/mm0/ansible-role-baseline)


An Ansible role that runs a few baseline tasks on a new server:

- Apt update
- Apt upgrade
- Install various default packages
- Install python passlib library
- Configure MOTD for ubuntu 14.04
- Sets default editor to vim
- Sets timezone
- Sets Hostname 
- Sets 127.0.0.1 {{ server_hostname }} entry in /etc/hosts



Requirements
---------------

- Sudo access


Role Variables
---------------

Available variables are listed below, there are no defaults:

```yml
  - server_hostname: localhost
  - timezone: America/Los_Angeles
  - extra_packages:
    - vim
    - lynx
```

Dependencies
---------------

None 

Example Playbook
---------------

```yml
- hosts: webservers
  vars:
  - server_hostname: localhost
  - timezone: America/Los_Angeles
  - extra_packages:
    - vim
    - lynx
  roles:
  - ansible-role-baseline
```
License
---------------

BSD-2


Author Information
------------------

[Matt Margolin](mailto:matt.margolin@gmail.com)

[mm0](https://github.com/mm0) on github