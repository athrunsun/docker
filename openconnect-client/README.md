# Openconnect client
A docker image based on Alpine with [OpenConnect](http://www.infradead.org/openconnect/) installed.

## Get started
Sample docker compose yaml configuration:
```yaml
version: '2'
services:
    openconnect_client:
        image: okampfer/openconnect-client
        container_name: openconnect_client
        devices:
            - "/dev/net/tun"
        networks:
            - ciscovpn_all_in_one
        privileged: true
        dns:
            - x.x.x.x
            - x.x.x.x
        dns_search: example.com
        cap_add:
            - NET_ADMIN
        extra_hosts:
            - "extra.com:x.x.x.x"
        # https://stackoverflow.com/a/30209974/1239295
        command: [tail, -f, /dev/null]
networks:
    ciscovpn_all_in_one:
```

