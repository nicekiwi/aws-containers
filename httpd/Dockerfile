ARG BASE_TAG=latest
FROM nicekiwi/aws-base:${BASE_TAG:-latest}

RUN yum install -y httpd mod_ssl

# Cleanup
RUN yum clean all

# https://httpd.apache.org/docs/2.4/stopping.html#gracefulstop
STOPSIGNAL SIGWINCH
