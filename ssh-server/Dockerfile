FROM gliderlabs/alpine
MAINTAINER Bruce Sun <okampfer@gmail.com>

RUN apk-install openssh && \
    echo "PasswordAuthentication yes" | tee -a /etc/ssh/sshd_config

CMD ["/usr/sbin/sshd", "-D", "-f", "/etc/ssh/sshd_config"]
