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
- ansible-roles:
```shell
ansible-roles inventory_name group_name role1 role2 role3
```
