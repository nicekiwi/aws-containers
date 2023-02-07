FROM nicekiwi/aws-base:latest

# Install PHP 8.1
RUN dnf install -y php8.1 php8.1-{cli,fpm,mysqlnd,pgsql,devel,gd,mbstring,xml,bcmath,opcache,intl,pdo}

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Cleanup
RUN dnf clean dbcache