ARG BASE_ARCH=arm64v8
ARG BASE_VERSION=2
FROM ${BASE_ARCH}/amazonlinux:${BASE_VERSION}

# Set timezone to UTC
RUN ln -snf /usr/share/zoneinfo/UTC /etc/localtime

# Update image
RUN yum update -y

# Install EPEL repository
RUN amazon-linux-extras install -y epel

# Update image
RUN yum update -y

# Install ZSH and utilities
RUN yum install -y git wget tar nano yum-utils telnet util-linux-user awscli zsh htop

# Set ZSH as default
RUN chsh -s /bin/zsh

# Install Oh my ZSH
RUN sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# copy local .zshrc to image
COPY .zshrc /root/.zshrc

# Cleanup
RUN yum clean all