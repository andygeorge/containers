# Artillery

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
podman run --rm -it -v ./example-config.yml:/root/nodestuff/config.yml

# in container
artillery run config.yml
```
