# rbc

> ### Remote scripts invoking
> By running command like: ``shell \curl -sSL http://www.domain.com/path | command``,
> you can run scripts and then run a batch script after downloading.

## Remote Bash Calls
This repo contains some bash scripts that are
ad-hoc, useful as well as rarely used.

### To RBC this repo:
Run command(replace ``certain_function`` with a script name in this repository):
```shell
\curl -sSL https://raw.githubusercontent.com/mccg/rbc/master/certain_function | bash
# or add arguments after '-s'
\curl -sSL https://raw.githubusercontent.com/mccg/rbc/master/certain_function | bash -s some args
```

## Features(functions) by now:
- ### Test ansible-roles by one line command:
```shell
ansible-roles <inventory path> <group name> <role1> [ role2, role3, ... ]
```
An example when ansible practice is as follows:
```shell
#   .
#   ├── ansible.cfg
#   ├── _a_playbook.yml
#   ├── inventories
#   │   ├── develop
#   │   │   └── hosts
#   │   └── staging
#   │       └── hosts
#   └── roles
#       └── role1
#           ├── tasks
#           │   └── main.yml
#           └── vars
#               └── main.yml
# Run:
ansible-roles inventories/staging group1 role1
```

