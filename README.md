# rbc
- ## Remote Bash Calls
  - This repo contains some bash scripts that are
    ad-hoc, useful as well as rarely used.
    
- ## How to remote call bash of this repository:
  - Run command(replace ``FX`` with a script name in this repository):
    ```shell
    \curl -sSL https://raw.githubusercontent.com/mccg/rbc/r/FX | bash
    # or add arguments after '-s'
    \curl -sSL https://raw.githubusercontent.com/mccg/rbc/r/FX | bash -s some args
    ```

- ## Features by now:
  - ### Test your ansible roles by one line command:
    ```shell
    ansible-roles <inventory_path> <group_name> <role1> [ role2, role3, ... ]
    ```
    When you create a ansible role, wirte a playbook to test it is redundant.
    `ansible-roles` helps you do that work.
    An example if your ansible practice likes as follows:
    
    ```shell
    #   .
    #   ├── ansible.cfg
    #   ├── _a_playbook.yml
    #   ├── inventories
    #   │   ├── develop
    #   │   └── staging
    #   └── roles
    #       ├── role1
    #       │   ├── tasks
    #       │   │   └── main.yml
    #       │   └── vars
    #       │       └── main.yml
    #       ├── role2
    #       ...
    #
    # Run:
    ansible-roles inventories/staging group1 role1
    ```

- > ### Remote scripts invoking
  > By running command like: ``\curl -sSL http://www.domain.com/path | command``,
    you will be able to run a batch script after downloading.
