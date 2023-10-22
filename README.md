# rsync-server

A dockerized `rsyncd` server.

## Start the server

```shell
docker run \
    --name rsync-server \
    -p 873:873 \
    -e USERNAME=username \
    -e PASSWORD=password \
    aggurio/rsync-server:latest
```
Variable options:

* `USERNAME` - `rsync` username. Defaults to `username`.
* `PASSWORD` - `rsync` password. Defaults to `password`.
* `VOLUME`   - the path for `volume` storage. Defaults to `/data`.

## Usage

```shell
rsync -av /your/folder/ rsync://username@localhost:8073/volume
```
