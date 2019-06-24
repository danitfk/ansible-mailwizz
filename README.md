Ansible MailWizz
=========
[![Build Status](https://travis-ci.org/danitfk/ansible-mailwizz.svg?branch=master)](https://travis-ci.org/danitfk/ansible-mailwizz)

This playbook prepare a complete environment to Install and Run [MailWizz  EMA](https://www.mailwizz.com/) system. 

## Features

- Prepare a fresh installed VM/Cloud/Droplet based on CentOS 7.x
- Install latest stable of MariaDB Server 10.4
- Install latest stable of NGINX Web Server
- Install PHP and requirements modules such as `gd,mbstring,tidy,pdo,phpiredis,etc..`
- Configure NGINX virtual host and PHP-FPM Pool optimized for MailWizz EMA
- Create user for MailWizz EMA and set necessary configuration for it
- Download and extract MailWizz EMA

Requirements
------------

- Fresh Install VM/Cloud with CentOS 7.x
- Proper access to the internet
- Open port for 80/443 
- User with sudo privilege 
- SSH Access to the Host
- Python Installed on machine

Variables and adjustments
--------------

You can made some adjustment and customization in variable file which located here: `$PROJECT_HOME/mailwizz/defaults/main.yml`

Dependencies
------------

There are no dependencies for this playbook.

Example Playbook
----------------

You can use this example to run this playbook.

```yaml
---
- hosts: all
  become: true
  roles:
  - mailwizz
```


