ansible-role-grub_cmdline
=========

Ansible role to template /etc/default/grub and then update grub afterwards.

Requirements
------------

None.

Role Variables
--------------

```
GRUB_CMDLINE_LINUX_DEFAULT: "quiet"
```

The following var is used in templates/grub.j2. I use it as I need different
values on different machines.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: richardskumat.ansible-role-grub_cmdline, GRUB_CMDLINE_LINUX_DEFAULT: "quiet" }

License
-------

GPLv3

Author Information
------------------

Richard Skumat

Link:

https://github.com/richardskumat
