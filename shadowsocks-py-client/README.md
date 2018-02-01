# shadowsocks-py-server
Docker version of [shadowsocks-py](https://pypi.python.org/pypi/shadowsocks-py), but only running a client.

See [here](https://github.com/gliderlabs/docker-alpine/blob/master/docs/usage.md#example) for a full example Dockerfile that installs the Python runtime and some build dependencies.

## Get started
Start a shadowsocks client which listens on port 10080 of your host machine:
```shell
docker run --name [container_name] -d -p 10080:1080 --link [shadowsocks_server_container_name]:ssserver okampfer/shadowsocks-py-client -s ssserver -p [server_port] -l 1080 -k $SSPASSWORD -m aes-256-cfb
```

NOTE it is highly recommended that you store the shadowsocks password in an environment variable as shown above. This way the password will not show in plain text when you run `docker ps`.
