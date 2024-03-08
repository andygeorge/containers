# `semaphore-pip-ansible`

This is based off the awesome [Ansible Semaphore](https://github.com/ansible-semaphore/semaphore/), and builds upon their existing Docker container by replacing the `apk`-managed Ansible installation with a `pip`-managed one, allowing for up to date Ansible installations.

### Build

```sh
SEMAPHORE_VERSION="v2.9.53-beta"
ANSIBLE_VERSION="9.3.0"
MY_VERSION="${SEMAPHORE_VERSION}_ansible-${ANSIBLE_VERSION}"

podman build --tag "localhost/semaphore-pip-ansible:testing" -f Containerfile
podman push "localhost/semaphore-pip-ansible:testing" "ghcr.io/andygeorge/semaphore-pip-ansible:$MY_VERSION"
podman push "localhost/semaphore-pip-ansible:testing" "ghcr.io/andygeorge/semaphore-pip-ansible:ansible-9"
podman push "localhost/semaphore-pip-ansible:testing" "ghcr.io/andygeorge/semaphore-pip-ansible:latest"

bash -c "while true; do podman push "localhost/semaphore-pip-ansible:testing" "ghcr.io/andygeorge/semaphore-pip-ansible:$MY_VERSION"; done"
```
