# `haskell`

## Building

```sh
podman build --tag "localhost/haskell:dev" -f Containerfile
podman push "localhost/haskell:dev" "ghcr.io/andygeorge/haskell:latest"
```

## Running

```sh
# on host
podman run --rm -it ghcr.io/andygeorge/haskell:latest
```
