ansible-role-fortiadc-backup
=========

Simple Ansible role to backup FortiADC configurations and send them to you via email.

Requirements
------------

In FortiADC:
- REST API User with globaladmin profile.

Dependencies
------------

-

Example Playbook
----------------

```
---

- name: Backup FortiADC configuration.
  hosts: all
  connection: local
  become: true
  gather_facts: false
  vars:
    mail:
      smtp_server: smtp.gmail.com
      smtp_port: 587
      recipient: contact@ndkprd.com
      sender: ansible@ndkprd.com

  roles:
    - ndkprd.fortiadc_backup

```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
