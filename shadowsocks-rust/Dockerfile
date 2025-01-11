FROM debian:bookworm-slim
MAINTAINER Bruce Sun <okampfer@gmail.com>

ADD https://github.com/shadowsocks/shadowsocks-rust/releases/download/v1.21.2/shadowsocks-v1.21.2.aarch64-unknown-linux-gnu.tar.xz

RUN apt-get update

RUN apt-get install -y \
  bash \
  curl \
  # ip command
  iproute2 \
  # ping command
  iputils-ping \
  # netstat command
  net-tools \
  # traceroute command
  traceroute
