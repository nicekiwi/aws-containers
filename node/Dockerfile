FROM nicekiwi/aws-base:latest

# Install NVM
RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash

RUN source ~/.zshrc

# Install and use Node.JS LTS
RUN nvm install --lts
RUN nvm use --lts

# Set LTS as default
RUN nvm alias default stable