Ansible grafana
=========

An ansible role for server monitoring using [grafana](https://github.com/grafana/grafana).

Requirements
------------

[Docker](https://www.docker.com/) must be installed on the server in order to use this role. If you don't have docker on your server we recommend [angstwad.docker_ubuntu](https://github.com/angstwad/docker.ubuntu) Ansible role.

Role Variables
--------------

```
# A password for admin user. You need it to login to the grafana.
gf_admin_password: paralect_drafana$
```

Dependencies
------------

[Docker](https://www.docker.com/) must be installed on the server in order to use this role. If you don't have docker on your server we recommend [angstwad.docker_ubuntu](https://github.com/angstwad/docker.ubuntu) Ansible role.

Example Playbook
----------------

```
---
- name: Deploy grafana monitoring
  hosts: monitoring
  become_user: root
  become: true
  roles:
    - role: paralect.grafana
      # A password for admin user. You need it to login to the grafana.
      gf_admin_password: paralect_drafana$
```

 License
 -------

 MIT
