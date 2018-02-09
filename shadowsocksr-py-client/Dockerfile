FROM gliderlabs/alpine:3.6
MAINTAINER Bruce Sun <okampfer@gmail.com>

RUN apk --no-cache add \
        python \
        python-dev

WORKDIR /shadowsocksr

ADD https://github.com/shadowsocksrr/shadowsocksr/archive/manyuser.zip ./ssr-manyuser.zip

RUN unzip ssr-manyuser.zip -d .

WORKDIR /shadowsocksr/shadowsocksr-manyuser

WORKDIR /shadowsocksr/shadowsocksr-manyuser/shadowsocks

ENTRYPOINT ["python", "client.py"]
