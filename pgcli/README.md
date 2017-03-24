# pgcli-docker
[pgcli](https://github.com/dbcli/pgcli) in a tiny Docker image powered by Alpine Linux

## How to use this image

Print help:

```shell
docker run --rm okampfer/pgcli-docker --help
```

Run pgcli:

```shell
docker run --rm -it --name=pgcli \
    --link=postgres:postgres \
    okampfer/pgcli-docker \
    postgresql://[user[:password]@][netloc][:port][/dbname]
```
