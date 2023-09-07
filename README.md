# containers

---

## `semaphore-pip-ansible`

This is based off the awesome [Ansible Semaphore](https://github.com/ansible-semaphore/semaphore/), and builds upon their existing Docker container by replacing the `apk`-managed Ansible installation with a `pip`-managed one, allowing for up to date Ansible installations.

### Build

```sh
podman build --tag "localhost/semaphore-pip-ansible:testing" -f Containerfile
podman push "localhost/semaphore-pip-ansible:testing" "ghcr.io/andygeorge/semaphore-pip-ansible:ansible-8.3.0"
```

---

## Artillery

Containerized [Artillery.io](https://www.artillery.io/) load testing (https://github.com/artilleryio/artillery).

### Building

```sh
podman build --tag "localhost/artillery:dev" -f Containerfile
podman push "localhost/artillery:dev" "ghcr.io/andygeorge/artillery:latest"
```

### Running

https://www.artillery.io/docs/

```sh
# on host
podman run -it ghcr.io/andygeorge/artillery:latest

# in container
artillery run example-config.yml
```
