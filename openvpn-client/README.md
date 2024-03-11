# Openvpn client
A docker image based on Alpine with OpenVPN installed.


# Get started
## Create and run a new container with the following command (assume you store your ovpn config file in your home folder somewhere), run with `--it` in case Google authentication code is required.

```sh
docker run --name <container_name> -p <shadowsocks_server_port>:<shadowsocks_server_port> -v $HOME:/mnt/host_system_home --cap-add=NET_ADMIN --device /dev/net/tun --privileged --dns <openvpn_dns_server> --dns-search <openvpn_dns_search_domain> --rm -it okampfer/openvpn-client-docker:alpine openvpn --config /path/to/some.ovpn --auth-user-pass /path/to/user_pass.txt
```

Command explanation:

- `--cap-add=NET_ADMIN --device /dev/net/tun --privileged`, see [dperson/openvpn-client](https://hub.docker.com/r/dperson/openvpn-client/).
- `--dns=IP_ADDRESS` (optional, can be used multiple times), sets the IP addresses added as nameserver lines to the container's `/etc/resolv.conf`, use it multiple times to specify more than 1 dns servers, also see [Configure container DNS](https://docs.docker.com/engine/userguide/networking/default_network/configure-dns/).
- `--dns-search=DOMAIN...` (optional), sets the domain names that are searched when a bare unqualified hostname is used inside of the container, by writing search lines into the container's `/etc/resolv.conf`.
- `--add-host` (optional), add a line to /etc/hosts (host:IP), also see [Docker run reference - Network settings](https://docs.docker.com/engine/reference/run/#network-settings).
- `/path/to/user_pass.txt` (optional, you'll get prompted if not provided), a file containing username on the 1st line and password on the 2nd line.
