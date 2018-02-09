FROM gliderlabs/alpine:3.6
MAINTAINER Bruce Sun <okampfer@gmail.com>

RUN apk --no-cache add \
        python \
        python-dev

WORKDIR /shadowsocksr

ADD https://github.com/shadowsocksrr/shadowsocksr/archive/manyuser.zip ./ssr-manyuser.zip

RUN unzip ssr-manyuser.zip -d .

WORKDIR /shadowsocksr/shadowsocksr-manyuser

# Refer to: https://github.com/shadowsocksrr/shadowsocksr/blob/manyuser/initcfg.sh
RUN chmod +x *.sh && \
    chmod +x shadowsocks/*.sh && \
    cp apiconfig.py userapiconfig.py && \
    cp config.json user-config.json && \
    cp mysql.json usermysql.json

WORKDIR /shadowsocksr/shadowsocksr-manyuser/shadowsocks

ENTRYPOINT ["python", "server.py"]
