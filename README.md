supervisor
============

The role installs supervisor and manages the config files. By default the role won't
make any changes on remote unless the variable supervisor is defined see details below.


Role Variables
--------------

A variable supervisor must be defined for the remote nodes, can be managed in group_vars or host_vars.

Example:

group_vars/eu-west-1a-app.yml

```
supervisor_conf: /etc/ansible/group_files/<hostgroup>/supervisor/supervisord.conf
supervisor_conf_d: /etc/ansible/group_files/<hostgroup>/supervisor/conf.d


OR Relative path


supervisor_conf: group_files/<hostgroup>/supervisor/supervisord.conf
supervisor_conf_d: group_files/<hostgroup>/supervisor/conf.d
```

All files in supervisord.conf_d ending with .conf extension will be copied to remot's  /etc/supervisor/conf.d


Author Information
------------------

Tal Lannder

tlannder@globeandmail.com
