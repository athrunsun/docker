FROM debian:bookworm-slim
MAINTAINER Bruce Sun <okampfer@gmail.com>

RUN apt-get update

RUN apt-get install -y \
  bash \
  curl \
  openvpn \
  # ip command
  iproute2 \
  # ping command
  iputils-ping \
  # netstat command
  net-tools \
  # traceroute command
  traceroute
