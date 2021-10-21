rnp-tools-ansible-roles-installdocker
=========

Ansible Role - Install docker

![Overwiew](https://raw.githubusercontent.com/rachuna-net-pl/rnp-tools-ansible-roles-installdocker/master/docs/installdocker.png)

Role Variables
--------------

Defaults role values:
```
input_role_os_distribution:               Ubuntu
input_role_os_distribution_major_version: "18"
input_docker_compose_url:                 https://github.com/docker/compose/releases/download/{{ var_docker_compose_version }}/docker-compose-Linux-x86_64
input_role_install_docker_compose:        yes
```

Role vars
```
var_docker_compose_version: "1.29.2"
var_docker_compose_path: "/usr/local/bin/docker-compose"
```

Example Playbook
----------------

```
  - hosts: localhost
    remote_user: root
    tasks:
    - include_role:
        name: rnp-tools-ansible-roles-installdocker
      vars:
        input_role_os_distribution:               "{{ ansible_distribution }}"
        input_role_os_distribution_major_version: "{{ ansible_distribution_major_version }}"
        input_role_install_docker_compose:        yes
```

License
-------

BSD 3-Clause

Author Information
------------------

### Maciej Rachuna
SysOps/DevOps