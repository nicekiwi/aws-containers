ARG ARCH=amd64
FROM nicekiwi/aws-base:${ARCH:-amd64}

RUN yum install -y httpd mod_ssl

# Cleanup
RUN yum clean all

# https://httpd.apache.org/docs/2.4/stopping.html#gracefulstop
STOPSIGNAL SIGWINCH
