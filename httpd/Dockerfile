FROM nicekiwi/aws-base:latest

RUN yum install -y httpd

# Cleanup
RUN yum clean all

# https://httpd.apache.org/docs/2.4/stopping.html#gracefulstop
STOPSIGNAL SIGWINCH
