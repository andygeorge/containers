# `fedora`

## Building

```sh
podman build --tag "localhost/fedora:dev" -f Containerfile
podman push "localhost/fedora:dev" "ghcr.io/andygeorge/fedora:latest"
```

## Running

```sh
# on host
podman run --rm -it ghcr.io/andygeorge/fedora:latest
```
