# ansible-role-docker-swarm
Ansible Role - Docker Swarm

## Role Variables
Available variables are listed below, along with default values (see `defaults/main.yml`):

```yml
docker_swarm_manager_group: 'docker_swarm_managers'
docker_swarm_worker_group: 'docker_swarm_workers'
```

## Use with Ansible (and docker Python library)

Many users of this role wish to also use Ansible to then build Docker images and manage Docker containers on the server where Docker is installed. In this case, you can easily add in the docker Python library using the geerlingguy.pip role:

```yml
- hosts: all

  vars:
    pip_install_packages:
      - name: docker
      - name: jsondiff

  roles:
    - soramitsukhmer.pip
    - soramitsukhmer.docker
```
