FROM amazonlinux:2.0.20230119.1

# Set timezone to UTC
RUN ln -sf /usr/share/zoneinfo/UTC /etc/localtime

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