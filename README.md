# rbc
---
## Remote scripts invoking
Running command like:
```shell
\curl -sSL http://name.of.domain/path | command
```
helps you download scripts and then run it.

## Remote Bash Calls
This repo contains some bash scripts that are 
ad-hoc, useful as well as rarely used.

### To RBC this repo:
Run command(replace ``certain_function`` with a scripts name in this repository):
```shell
\curl -sSL https://raw.githubusercontent.com/mccg/rbc/master/certain_function | bash
# or add arguments after '-s'
\curl -sSL https://raw.githubusercontent.com/mccg/rbc/master/certain_function | bash -s some args
```

## Features(functions) by now:


