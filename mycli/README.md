# mycli-docker
[mycli](https://github.com/dbcli/mycli) in a tiny Docker image powered by Alpine Linux

## How to use this image

Print help:

```bash
docker run --rm okampfer/mycli-docker --help
```

Run mycli:

```bash
docker run --rm -ti --name=mycli \
  --link=mysql:mysql \
  okampfer/mycli-docker \
  --host=mysql \
  --port=3306 \
  --database=mysql \
  --user=root \
  --password=secret
```
