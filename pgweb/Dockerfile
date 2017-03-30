FROM gliderlabs/alpine
MAINTAINER Bruce Sun <okampfer@gmail.com>

ADD entrypoint.sh /entrypoint.sh
ENV PGWEB_VERSION 0.9.6
ENV BIND_ADDRESS 0.0.0.0
ENV LISTEN_PORT 8080

RUN apk-install ca-certificates && \
  update-ca-certificates && \
  cd /tmp && \
  wget https://github.com/sosedoff/pgweb/releases/download/v$PGWEB_VERSION/pgweb_linux_amd64.zip && \
  unzip pgweb_linux_amd64.zip -d /usr/bin && \
  mv /usr/bin/pgweb_linux_amd64 /usr/bin/pgweb && \
  rm -f pgweb_linux_amd64.zip

ENTRYPOINT ['/entrypoint.sh']
