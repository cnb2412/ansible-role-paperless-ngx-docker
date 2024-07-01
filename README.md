Role Name
=========

Ansible role to run and manage paperless-ngx in a Docker environment.

Role Variables
--------------
| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `paperless_ngx_docker_install`| true | Install paperless-ngx, false will remove everything |
| `paperless_ngx_docker_basedir` | /opt/paperless-ngx | Path to basedir where paperless-ngx folder structure is created, which will be mounted into the container |
| `paperless_ngx_docker_group_host`| root | Name of the group with wich the container is running. |
| `paperless_ngx_docker_user_host`| root | Name of the user with wich the container is running. |
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
| `paperless_ngx_docker_reverse_proxy_enable`| false | Should a reverse proxy container (NGINX) should be setup. |
| `paperless_ngx_docker_reverse_proxy_image`| docker.io/library/nginx:stable-alpine-slim | NGIX image that shoud be used. |
| `paperless_ngx_docker_reverse_proxy_container_name`| paperless-nginx | Name of the NGINX container that is started, if reverse proxy is enabled. |
| `paperless_ngx_docker_reverse_proxy_path`| "{{ paperless_ngx_docker_basedir }}/nginx" | Path to volume where NGINX config is stored, i.e. mounted in Docker container. A nginx.conf file must exist in this directory  |
| `paperless_ngx_docker_reverse_proxy_ssl_key`| "" | Path to TLS Cert private key. Both cert and key must configured to enable TLS. |
| `paperless_ngx_docker_reverse_proxy_ssl_cert`| "" | Path to TLS Cert. Both cert and key must configured to enable TLS. |
| `paperless_ngx_docker_app_image`| ghcr.io/paperless-ngx/paperless-ngx:latest | Paperless-ngx image that shoud be used. |
| `paperless_ngx_docker_app_container_name`| paperless-ngx | Name of the paperless-ngx container that is started. |


License
-------

BSD
