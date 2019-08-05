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

  - ### Tree of content
    - [rm-namechar](#rm-namechar)
    - [file-prefix](#file-prefix)
    - [ansible-roles](#ansible-roles)
    - [seq-tm](#seq-tm)

  <span id="rm-namechar"></span>
  - ### Remove useless characters of file/directory name
    It will remove bytes in file/directory name like '`` ``', '``?``', '``%``'..., in the meantime keep '``.``' and '``-``'.

    ```shell
    rm-namechar [OPTION]...
    ```
    | Argument          | Comment                                   |
    | ---               | ---                                       |
    | -d                | Only search directories.                  |
    | -f                | Only search files.                        |
    | -r                | Search directory and files. (Default)     |
    | --max\|--maxdepth | Maximum depth of searching. (Default: 5)  |
    | --min\|--mindepth | Minimum depth of searching. (Default: 1)  |
    | -p\|--pattern     | Files pattern of searching.               |
    | --pattern-dir |  Directories pattern of searching.            |
    Quick copy:
    ```shell
    \curl -sSL https://raw.githubusercontent.com/mccg/rbc/r/rm-namechar | bash -s
    ```

  <span id="file-prefix"></span>
  - ### Organize prefix of files in directory
    ```shell
    file-prefix [-m|--mark <mark>] [-d|--digit <digits>]
    ```
    Quick copy:
    ```shell
    \curl -sSL https://raw.githubusercontent.com/mccg/rbc/r/file-prefix | bash -s
    ```

  <span id="ansible-roles"></span>
  - ### Test your ansible roles by one line command
    ```shell
    ansible-roles <inventory_path> <group_name> <role1> [ role2, role3, ... ]
    ```
    After creating an ansible role, wirting a playbook to test it is redundant.
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
    Quick copy:
    ```shell
    \curl -sSL https://raw.githubusercontent.com/mccg/rbc/r/ansible-roles | bash -s
    ```

  <span id="seq-tm"><span>
  - ### Generate a datetime string array by `date` in shell 
    Given a begin datetime, an end datetime, timedelta and output format,
    an array could be generated in shell environment.

    ```shell
    seq-tm <date_command>[.d] "<begin_datetime>" "<end_datetime>" "<time_delta>" "<output_format>"
    ```
    | Argument       | Comment                                            | Examples |
    | ---            | ---                                                | :---:    |
    | `date_command` | 'date' in most cases, 'gdate' in BSD and MacOS.    | `date`, `gdate`
    | `.d`           | Debug mode will print result sequence and etc.     | `date.d`
    | begin_datetime | Datetime format arguments in `date`'s `-d` option. | `2017-09-01 08:00:00 +0800`
    | end_datetime   | Ditto.                                             | `2017-09-02`
    | time_delta     | Time delta in `date`'s `-d` option.                | `+1 day`, `-2 min`
    | output_format  | Format in     `date`'s `+` option.                 | `%Y-%m-%d %H:%M:%S`

    Quick copy:
    ```shell
    \curl -sSL https://raw.githubusercontent.com/mccg/rbc/r/seq-tm | bash -s
    ```

- > ### Remote scripts invoking
  > By running command like: ``\curl -sSL http://www.domain.com/path | command``,
    you will be able to run a batch script after downloading.
