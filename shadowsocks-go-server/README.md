# Shadowsocks go server inside docker
A docker image based on alpine linux with a [shadowsocks-go](https://github.com/shadowsocks/shadowsocks-go) server binary inside.

## Get started
Please refer to [shadowsocks-go](https://github.com/shadowsocks/shadowsocks-go) official documentation for runtime arguments (`-p`, `-m`, etc.).
```shell
docker run --rm --name <container_name> -d -p <shadowsocks_server_port>:<shadowsocks_server_port> okampfer/shadowsocks-go-server-docker -p <shadowsocks_server_port> -m <encryption_method> -k <password> ...
```
