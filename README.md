Ansible Role : ball6847.python
==============================

Very simple role to install python-minimal on your **ubuntu** box,
enable you to run advanced ansible module on server.

Installation
------------

```sh
ansible-galaxy install git+https://github.com/ball6847/ansible-role-python.git,master
```

or by requirements.yml then do `ansible-galaxy install -r requirements.yml`

```yml
# requirements.yml commingsoon
```

Playbook Example
----------------

```yml
# python.yml
- name: "Install python"
  hosts: all
  gather_facts: no
  roles:
    - ball6847.python
```

 **IMPORTANT**:

`gather_facts: no` is neccessary since `gather_facts: yes` (which is `yes` by default) requires python to be installed on remote machine.
