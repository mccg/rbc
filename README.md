# rbc

### To RBC this repository:
Run command(replace ``FX`` with a script name in this repository):
```shell
\curl -sSL https://raw.githubusercontent.com/mccg/rbc/r/FX | bash
# or add arguments after '-s'
\curl -sSL https://raw.githubusercontent.com/mccg/rbc/r/FX | bash -s some args
# or using a shorter URL from rawgit.com
\curl -sSL https://rawgit.com/mccg/rbc/r/FX | bash -s
```

## Features(functions) by now:
- ### Test ansible-roles by one line command:
```shell
ansible-roles <inventory_path> <group_name> <role1> [ role2, role3, ... ]
```
An example if your ansible practice likes as follows:
```shell
#   .
#   ├── ansible.cfg
#   ├── _a_playbook.yml
#   ├── inventories
#   │   ├── develop
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

## Remote Bash Calls
This repo contains some bash scripts that are
ad-hoc, useful as well as rarely used.

> ### Remote scripts invoking
> By running command like: ``\curl -sSL http://www.domain.com/path | command``,
> you can run scripts and then run a batch script after downloading.
