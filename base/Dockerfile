FROM amazonlinux:2022

# Set timezone to UTC
RUN ln -sf /usr/share/zoneinfo/UTC /etc/localtime

# Install ZSH and utilities
RUN dnf install -y git wget util-linux-user awscli zsh htop

# Set ZSH as default
RUN chsh -s /bin/zsh

# Install Oh my ZSH
RUN sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# copy local .zshrc to image
COPY .zshrc /root/.zshrc