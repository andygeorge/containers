# `semaphore-pip-ansible`

This is based off the awesome [Ansible Semaphore](https://github.com/ansible-semaphore/semaphore/), and builds upon their existing Docker container by replacing the `apk`-managed Ansible installation with a `pip`-managed one, allowing for up to date Ansible installations.

### Build

```sh
podman build --tag "localhost/semaphore-pip-ansible:testing" -f Containerfile
podman push "localhost/semaphore-pip-ansible:testing" "ghcr.io/andygeorge/semaphore-pip-ansible:v2.9.39-beta_ansible-8.3.0"
```
