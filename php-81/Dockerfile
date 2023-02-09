ARG ARCH=arm64
FROM nicekiwi/aws-base:${ARCH}

# Install PHP 8.1
RUN amazon-linux-extras install -y php8.1

# Install PHP extensions
RUN yum install -y php-{mysqlnd,pgsql,devel,gd,mbstring,xml,bcmath,opcache,intl,pdo,zip,opcache,redis,exif,calendar,soap,gettext,pcntl}

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Cleanup
RUN yum clean all