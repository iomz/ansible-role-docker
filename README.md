# ansible-role-docker

## `files/<host>/opt/dockers/<service-name>`

- this directory requires at least a docker-compose.yml
- this directory will be copied to the designated host

## `docker` config in `inventories/host_vars/<host>`

- if `build: true` then Ansible will build the image from the `Dockerfile` in the <serivce-name> directory

```yml
docker:
  images:
    - name: <service-name>
      build: yes/no
```

To deploy containers:

```bash
ansible-playbook
```
