ansible-role-docker-swarm
=========

![Ansible Role](https://img.shields.io/ansible/role/42991)
![Ansible Quality Score](https://img.shields.io/ansible/quality/42991)

Setup a Docker Swarm Cluster



Requirements
------------

- Ansible >=2.8.0

If your OS has Python 2 and Python 3 installed, Ansible may default to Python2. This role expects Python 3 so you may need to set `ansible_python_interpreter: /usr/bin/python3`

Example Playbook
----------------

Here is a simple example for using this role.



    - hosts: servers
      roles:
         - role: blue271828.docker_swarm



To set up a swarm cluster, you need to group hosts in an inventory file as follows for distinguishing them.

```
[docker_swarm_manager]
dkrmgr[01:03]

[docker_swarm_worker]
dkrwkr[01:03]

[docker_engine:children]
docker_swarm_manager
docker_swarm_worker
```



License
-------

[MIT](https://github.com/blue271828/ansible-role-docker-swarm/blob/master/LICENSE)


