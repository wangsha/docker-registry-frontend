docker-registry-frontend
============

[![Build Status](https://travis-ci.org/wangsha/docker-registry-frontend.svg?branch=master)](https://travis-ci.org/wangsha/docker-registry_frontend)
[![Ansible Galaxy](https://img.shields.io/badge/AnsibleGalaxy-wangsha.docker--registry--frontend-blue.svg)](https://galaxy.ansible.com/wangsha/docker-registry-frontend/)

Ansible role to manage and run the registry_frontend docker container.

Requirements
------------

This role has only been tested on Ubuntu 14.04. Since this uses Ansible's
docker module, you will need to ensure that a recent-ish version of `docker-py`
and `docker` are installed.

Examples
--------

Install this module from Ansible Galaxy into the './roles' directory:
```bash
ansible-galaxy install wangsha.docker-registry-frontend -p ./roles
```

Use it in a playbook as follows, assuming you already have docker setup:
```yaml
- hosts: 'servers'
  roles:
    - role: angstwad.docker_ubuntu
      become: true
    - role: wangsha.docker-registry-frontend
      become: true
```

Have a look at the [defaults/main.yml](defaults/main.yml) for role variables
that can be overridden.


If you need a playbook to set Docker itself, have a look at [angstwad.docker_ubuntu](https://github.com/angstwad/docker.ubuntu) Galaxy
role.


Additional References
---------------------
- [default docker image](https://hub.docker.com/r/konradkleine/docker-registry-frontend/)


License
-------

[MIT](LICENSE.txt)

Author Information
------------------

- wangsha
