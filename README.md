Ansible Role : ball6847.role.python
==============================

Very simple role to install python-minimal on your **ubuntu** box,
enable you to run advanced ansible module on server.

Installation
------------

```sh
ansible-galaxy install git+https://github.com/ball6847/ball6847.role.python.git,master
```

or by requirements.yml then do `ansible-galaxy install -r requirements.yml`

```yml
- src: https://github.com/ball6847/ball6847.role.python.git
  version: master
```

Playbook Example
----------------

```yml
# python.yml
- name: "Install python"
  hosts: all
  gather_facts: no
  roles:
    - ball6847.role.python
```

 **IMPORTANT**:

`gather_facts: no` is neccessary since `gather_facts: yes` (which is `yes` by default) requires python to be installed on remote machine.

Variables
---------

**python_package**:

name of python package you want to install (default: `python-minimal`), you might need to change this to something like `python-dev` if your system relies on python development package.
