ansible-role-homebrew
=====================

[![GitHub license](https://img.shields.io/github/license/bluk/ansible-role-homebrew.svg)](https://github.com/bluk/ansible-role-homebrew/blob/master/LICENSE) [![Build Status](https://travis-ci.org/bluk/ansible-role-homebrew.svg?branch=master)](https://travis-ci.org/bluk/ansible-role-homebrew)

An [Ansible](https://www.ansible.com) role to install and upgrade Homebrew taps
and packages.

Requirements
------------

It is assumed Homebrew is already installed.

Role Variables
--------------

* `homebrew_taps` - A list of dictionaries of Homebrew taps. The dictionary must contain a `name` key with the tap name as the value.

* `homebrew_packages` - A list of dictionaries of Homebrew packages. The dictionary must contain a `name` key with the package name as the value.

* `homebrew_casks` - A list of dictionaries of Homebrew casks. The dictionary must contain a `name` key with the cask name as the value.

* `homebrew_update` - A boolean describe if Homebrew should update.

* `homebrew_upgrade` - A boolean describe if Homebrew should upgrade existing packages.

Dependencies
------------

No dependencies.

Example Playbook
----------------

```
- hosts: servers
  roles:
     - { role: bluk.homebrew }
```

License
-------

Apache 2.0
