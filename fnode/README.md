# `fnode`

## Building

```sh
podman build --tag "localhost/fnode:dev" -f Containerfile
podman push "localhost/fnode:dev" "ghcr.io/andygeorge/fnode:latest"
```

## Running

```sh
# on host
podman run --rm -it -v ./:/root/nodestuff/ ghcr.io/andygeorge/fnode:latest
```
