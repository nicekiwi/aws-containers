FROM nicekiwi/aws-base:latest

RUN dnf install -y httpd

# Cleanup
RUN dnf clean dbcache

# https://httpd.apache.org/docs/2.4/stopping.html#gracefulstop
STOPSIGNAL SIGWINCH
