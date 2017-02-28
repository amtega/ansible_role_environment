# Ansible environment role

Environment is an [Ansible](http://www.ansible.com) role which adds `/etc/environment` variables

## Dependencies

- Ansible >= 2.0

## Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```yaml
---

# Path to the environment file

environment_file: /etc/environment

# The environment file owner

environment_file_owner: root

# The environment file group

environment_file_group: root

# The environment file permissions mode

environment_file_mode: 644

# Dictionary of environment variables
#
# Sample:
#
# environment_config:
#   LC_ALL: en_US.UTF-8

environment_config:
```

## Usage

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - environment:
  vars:
    environment_config:
      LC_ALL: C
```

## Testing

```shell
$ git clone https://github.com/weareinteractive/ansible-environment.git
$ cd ansible-environment
$ make test
```
