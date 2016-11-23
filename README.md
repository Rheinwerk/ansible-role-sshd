SSHD Setup
=========

This role can be used to set up OpenSSH's `sshd_config`.
It allows the configuration of trusted Root CA keys, allowed user and
groups etc.

[![Build Status](https://travis-ci.org/Rheinwerk/ansible-role-sshd.svg?branch=master)](https://travis-ci.org/Rheinwerk/ansible-role-sshd)

Requirements
------------
None

Role Variables
--------------

There is one main variable that drives this role: `_sshd`. It is a map that contains all configuration and settings for this role.
Please see `defaults/main.yml` for details.

Dependencies
------------

None.


Example Playbook
----------------

The general contract of this role is to take the variables map `_sshd` from `defaults/main.yml` as a template for your configuration and pass that configuration as a parameter to this role.

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      var:
        SSHD:
          ...
      roles:
         - { role: sshd, tags: [ 'sshd' ], _sshd: "{{ SSHD_SETUP }}" }

License
-------

Please see LICENSE.

Author Information
------------------

Original author is [Daniel Schneller](https://github.com/dschneller) as member of the [Rheinwerk](https://github.com/Rheinwerk) project.

