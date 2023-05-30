# ansible-role-docker

Setting up Docker on your host

## Requirements

None.

## Role Variables

Put `docker` variable in `inventories/host_vars/<host>`

- if `build: true` then Ansible will build the image from the `Dockerfile` in the <serivce-name> directory

```yml
docker:
  images:
    - name: <service-name>
      build: <bool>
```

## Optional: directories for docker compose

`files/<host>/opt/dockers/<service-name>`

- this directory should contain `docker-compose.yml`
- this directory will be copied to the designated host

## Example Playbook

```yml
- hosts: servers
  roles:
    - { role: iomz.docker }
```

## Dependencies

None.

## License

MIT

## Author Information

[@iomz](https://github.com/iomz) (Iori Mizutani)
