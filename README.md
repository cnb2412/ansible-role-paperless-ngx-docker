Role Name
=========

Ansible role to run and manage paperless-ngx in a Docker environment.

Role Variables
--------------
| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `paperless_ngx_docker_basedir` | /opt/paperless-ngx | Path to basedir where paperless-ngx folder structure is created, which will be mounted into the container |
| `paperless_ngx_docker_install`| true | Install paperless-ngx, false will remove everything |


License
-------

BSD
