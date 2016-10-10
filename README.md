# README.md

# Ansible Role: Baseline v1.0

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



See Also: 

![travis-ci](https://travis-ci.org/mm0/ansible-role-baseline.svg?branch=master)

## Requirements

- Sudo access


## Role Variables

Available variables are listed below, there are no defaults:

      - server_hostname: localhost
      - timezone: America/Los_Angeles
      - extra_packages:
        - vim
        - lynx

## Dependencies

None 

## Example Playbook

    - hosts: webservers
      vars:
      - server_hostname: localhost
      - timezone: America/Los_Angeles
      - extra_packages:
        - vim
        - lynx
      roles:
      - ansible-role-baseline

## License

MIT


Author Information
------------------

[Matt Margolin](mailto:matt.margolin@gmail.com)

mm0 on github
