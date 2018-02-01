FROM gliderlabs/alpine:3.6
MAINTAINER Bruce Sun <okampfer@gmail.com>

RUN apk --no-cache add \
        python \
        python-dev \
        py-pip \
        build-base
RUN pip install shadowsocks-py==2.9.1

ENTRYPOINT ["sslocal"]
