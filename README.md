Reboot if required
=========

An ansible role for rebooting Linux hosts when a reboot is required.

Requirements
------------

- Just the python interpreter

Role Variables
--------------

Variable | Description | Default
--- | --- | ---
`reboot_allowed`| Is a reboot allowed? | False
`reboot_time`| Difine a reboot time like in "HH:MM" or "+5" for in 5 minutes. Lookup "man shutdown" for further information. If you want to reboot instantly, ignore these variable.  | undefined

Dependencies
------------

None.

Example Playbook
----------------

Reboot in 10 minutes:

```yaml
---
- hosts: all
  vars:
    reboot_allowed: True
    reboot_time: '+10'
  roles:
    - ansible-reboot-required
```

License
-------

GPL3
