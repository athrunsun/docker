# Shadowsocks go client inside docker
A docker image based on alpine linux with a [shadowsocks-go](https://github.com/shadowsocks/shadowsocks-go) client binary inside.

## Get started
Please refer to [shadowsocks-go](https://github.com/shadowsocks/shadowsocks-go) official documentation for runtime arguments (`-p`, `-m`, etc.).
```shell
docker run --rm --name <container_name> -d -p <shadowsocks_client_port>:<shadowsocks_client_port> okampfer/shadowsocks-go-client-docker -s <server_address> -p <shadowsocks_server_port> -b <shadowsocks_client_address> -l <shadowsocks_client_port> -m <encryption_method> -k <password> ...
```
