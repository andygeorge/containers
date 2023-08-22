# `artillery`

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
