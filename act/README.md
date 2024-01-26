# `act`

## Building

```sh
podman build --format docker --tag "localhost/act:dev" -f Containerfile
podman push "localhost/act:dev" "ghcr.io/andygeorge/act:ubuntu-22.04"
```

## Running

```sh
# on host
sudo AWS_ACCESS_KEY_ID=$AWS_ACCESS_KEY_ID AWS_SECRET_ACCESS_KEY=$AWS_SECRET_ACCESS_KEY act \
	-s AWS_ACCESS_KEY_ID -s AWS_SECRET_ACCESS_KEY \
	-P ubuntu-22.04=ghcr.io/andygeorge/act:ubuntu-22.04 \
	--artifact-server-path tmp/artifacts
```
