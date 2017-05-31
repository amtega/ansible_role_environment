# Ansible environment role

Environment is an [Ansible](http://www.ansible.com) role which adds `/etc/environment` variables

## Dependencies

- Ansible >= 2.0

## Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

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

Test are based on docker containers. You can run the tests with the following commands:

```shell
$ cd environment/test
$ ansible-playbook main.yml
```

If you have docker engine configured you can avoid running dependant 'docker_engine' role (that usually requries root privileges) with the following commands:

```shell
$ cd environment/test
$ ansible-playbook --skip-tags "role::docker_engine" main.yml
```

## License

Not defined.

## Author Information

- Juan Antonio Valiño García ([juanval@edu.xunta.es](mailto:juanval@edu.xunta.es)). Amtega - Xunta de Galicia
