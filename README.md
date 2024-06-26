Role Name
=========

Ansible role to run and manage paperless-ngx in a Docker environment.

Role Variables
--------------
| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `paperless_ngx_docker_install`| true | Install paperless-ngx, false will remove everything |
| `paperless_ngx_docker_basedir` | /opt/paperless-ngx | Path to basedir where paperless-ngx folder structure is created, which will be mounted into the container |
| `paperless_ngx_docker_group_host`| paperless | Name of the group that is created on the host system. If empty, no group will be created. Docker container user will use this group, if set. |
| `paperless_ngx_docker_user_host`| paperless | Name of the user that is created on the host system. If empty, no user will be created. Docker container user will use this group, if set. |
| `paperless_ngx_docker_dedicated_docker_network_name`| "" | Name of Docker network, which is created for the container. If empty, no extra network is created and the default one is ued. |
| `paperless_ngx_docker_redis_image`| docker.io/library/redis:7 | Redis image that shoud be used. |
| `paperless_ngx_docker_redis_container_name`| paperless-redis | Name of the redis container that is started. |
| `paperless_ngx_docker_redis_path`| {{ paperless_ngx_docker_basedir }}/redis | Path to volume where redis data is stored, i.e. mounted in Docker container |
| `paperless_ngx_docker_db_image`| docker.io/library/postgres:latest | Database image that shoud be used. |
| `paperless_ngx_docker_db_container_name`| paperless-db | Name of the database container that is started. |
| `paperless_ngx_docker_db_path`| "{{ paperless_ngx_docker_basedir }}/database" | Path to volume where database data is stored, i.e. mounted in Docker container |
| `paperless_ngx_docker_db_name`| paperless | DB name for paperless |
| `paperless_ngx_docker_db_user`| paperless | DB user for paperless |
| `paperless_ngx_docker_db_password`| changeme | DB password that is used. Must be changed. |

License
-------

BSD
