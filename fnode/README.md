# `fnode`

## Building

```sh
export NODE_VERSION=latest
export NODE_VERSION=lts

podman build --tag "localhost/fnode:$NODE_VERSION" --build-arg NODE_VERSION -f Containerfile
podman push "localhost/fnode:$NODE_VERSION" "ghcr.io/andygeorge/fnode:$NODE_VERSION"
```

## Running

```sh
# on host
podman run --rm -it -v ./:/root/nodestuff/ ghcr.io/andygeorge/fnode:latest
podman run --rm -it -v ./:/root/nodestuff/ ghcr.io/andygeorge/fnode:lts
podman run --rm -it -v ./:/root/nodestuff/ ghcr.io/andygeorge/fnode:23
podman run --rm -it -v ./:/root/nodestuff/ ghcr.io/andygeorge/fnode:20
podman run --rm -it -v ./:/root/nodestuff/ ghcr.io/andygeorge/fnode:18
```
