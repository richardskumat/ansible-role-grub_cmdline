ansible-role-grub_cmdline
=========

Ansible role to template /etc/default/grub and then update grub afterwards.

Requirements
------------

None.

Role Variables
--------------

On 2023-03-12, this default variable has been changed to the lower
case version of its former self. Changed due to ansible-lint:

'var-naming: File defines variable 'GRUB_CMDLINE_LINUX_DEFAULT' that violates variable naming standards'

```bash
# changes GRUB_CMDLINE_LINUX_DEFAULT to lowercase word
echo 'GRUB_CMDLINE_LINUX_DEFAULT' | tr [:upper:] [:lower:]
```

```
grub_cmdline_linux_default: "quiet"
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
