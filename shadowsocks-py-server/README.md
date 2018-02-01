# shadowsocks-py-server
Docker version of [shadowsocks-py](https://pypi.python.org/pypi/shadowsocks-py), but only running a server.

See [here](https://github.com/gliderlabs/docker-alpine/blob/master/docs/usage.md#example) for a full example Dockerfile that installs the Python runtime and some build dependencies.

## Get started
Start a shadowsocks server which listens on port 10080 of your host machine:
```shell
docker run --name [container_name] -d -p 10080:1080 okampfer/shadowsocks-py-server -s 0.0.0.0 -p 1080 -k $SSPASSWORD -m aes-256-cfb
```

NOTE it is highly recommended that you store the shadowsocks password in an environment variable as shown above. This way the password will not show in plain text when you run `docker ps`.
