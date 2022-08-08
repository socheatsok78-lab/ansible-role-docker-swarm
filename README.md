# ansible-role-docker-swarm
Ansible Role - Docker Swarm

## Role Variables
Available variables are listed below, along with default values (see `defaults/main.yml`):

```yml
docker_swarm_manager_group: 'docker_swarm_managers'
docker_swarm_worker_group: 'docker_swarm_workers'
```

## Use with Ansible (and docker Python library)

Example:

```yml
- hosts: all

  vars:
    pip_install_packages:
      - name: docker
      - name: jsondiff

  roles:
    - soramitsukhmer-lab.pip
    - soramitsukhmer-lab.docker
```
