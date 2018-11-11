Common Linux Commands
=========

Installs commonly used commands and programs.

Requirements
------------

When using this role on a RedHat EL server, the EPEL repository is required. The task to install the additional repository may be added as a task or you can use the [Extra Repositories]() role.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: DebianHosts
  vars:
    common_linux_commands_extra:
      - gedit
      - vagrant
  roles:
   - the-paulus.common-linux-commands
```

```yml
- hosts: GentooHosts
  vars:
    common_linux_commands_gentoo_extra:
      - name: dev-vcs/subversion
        useflags:
          - perl
        remove_useflags:
          - dso
  roles:
   - the-paulus.common-linux-commands
```

License
-------

BSD
