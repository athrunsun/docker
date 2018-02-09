# shadowsocksr-py-server
Docker version of [shadowsocksr](https://github.com/shadowsocksrr/shadowsocksr), but only running a client.

See [here](https://github.com/gliderlabs/docker-alpine/blob/master/docs/usage.md#example) for a full example Dockerfile that installs the Python runtime and some build dependencies.

## Get started
Start a shadowsocksr client which listens on port 10080 of your host machine:
```shell
docker run --name [container_name] -d -p 10080:1080 --link [shadowsocksr_server_container_name]:ssrserver okampfer/shadowsocksr-py-client -s ssrserver -p [server_port] -l 1080 -k $SSRPASSWORD -m aes-256-cfb -O auth_aes128_sha1 -o tls1.2_ticket_auth
```

NOTE it is highly recommended that you store the shadowsocks password in an environment variable as shown above. This way the password will not show in plain text when you run `docker ps`.
